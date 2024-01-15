<script lang="ts">
    import * as Avatar from "$lib/components/ui/avatar";
    import { Button } from "$lib/components/ui/button";
    import * as Command from "$lib/components/ui/command";
    import * as Dialog from "$lib/components/ui/dialog";
    import * as Popover from "$lib/components/ui/popover";
    import { Textarea } from "$lib/components/ui/textarea";
    import { cn } from "$lib/utils";
    import { CaretSort, Check } from "radix-icons-svelte";
    import { tick } from "svelte";
    import Icon from 'svelte-icons-pack/Icon.svelte';
    import AiOutlineArrowLeft from "svelte-icons-pack/ai/AiOutlineArrowLeft";
    import Map from './Map.svelte';
 
    const categories = [
    {
      value: "cat",
      label: "Cat"
    },
    {
      value: "dog",
      label: "Dog"
    },
    {
      value: "rodent",
      label: "Rodent"
    },
    {
      value: "fish",
      label: "Fish"
    },
    {
      value: "bird",
      label: "Bird"
    },
    {
      value: "exotic-pet",
      label: "Exotic Pet"
    },
    {
      value: "other",
      label: "Other"
    }
  ];
  let open = false;
  let value = "";
  $: selectedValue =
    categories.find((f) => f.value === value)?.label ?? "Select a pet category...";
  // We want to refocus the trigger button when the user selects
  // an item from the list so users can continue navigating the
  // rest of the form with the keyboard.
  function closeAndFocusTrigger(triggerId: string) {
    open = false;
    tick().then(() => {
      document.getElementById(triggerId)?.focus();
    });
  }
</script>



<div>
    <div class="h-14 w-full flex flex-col">
        <div class="flex items-center justify-between h-full w-full p-4">
            <div><a href="/"><Icon src={AiOutlineArrowLeft} size="20"/></a></div>
            <div><Button class="rounded-full font-bold bg-[#02CD9F]">Post</Button></div>
        </div>
        <div class="px-4">
            <div class="flex flex-row min-h-40">
                <div class="pt-3 mr-3">
                    <Avatar.Root class="size-10">
                        <Avatar.Image src="https://github.com/shadcn.png" alt="@shadcn" />
                        <Avatar.Fallback>CN</Avatar.Fallback>
                    </Avatar.Root>
                </div>
                <div class="w-full pt-1">
                    <div class="pb-3">
                        <Popover.Root bind:open let:ids>
                            <Popover.Trigger asChild let:builder>
                              <Button
                                builders={[builder]}
                                variant="outline"
                                role="combobox"
                                aria-expanded={open}
                                class="w-[200px] justify-between"
                              >
                                {selectedValue}
                                <CaretSort class="ml-2 h-4 w-4 shrink-0 opacity-50" />
                              </Button>
                            </Popover.Trigger>
                            <Popover.Content class="w-[200px] p-0">
                              <Command.Root>
                                <Command.Input placeholder="Search category..." class="h-9" />
                                <Command.Empty>No category found.</Command.Empty>
                                <Command.Group>
                                  {#each categories as categories}
                                    <Command.Item
                                      value={categories.value}
                                      onSelect={(currentValue) => {
                                        value = currentValue;
                                        closeAndFocusTrigger(ids.trigger);
                                      }}
                                    >
                                      <Check
                                        class={cn(
                                          "mr-2 h-4 w-4",
                                          value !== categories.value && "text-transparent"
                                        )}
                                      />
                                      {categories.label}
                                    </Command.Item>
                                  {/each}
                                </Command.Group>
                              </Command.Root>
                            </Popover.Content>
                          </Popover.Root>
                    </div>
                    <div class="py-3">
                        <Textarea placeholder="Please describe your missing pet: breed, color, distinctive markings, and any other relevant details." class="min-h-24 w-full"/>
                    </div>
                    <div>
                      <div>
                        <Dialog.Root>
                          <Dialog.Trigger>Last Location</Dialog.Trigger>
                          <Dialog.Content><Map/></Dialog.Content>
                        </Dialog.Root>
                      </div>
                      <div>
                        <p></p>
                      </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
