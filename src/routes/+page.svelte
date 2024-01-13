<script lang='ts'>
    import * as Avatar from "$lib/components/ui/avatar";
    import * as Sheet from "$lib/components/ui/sheet";
    import Icon from 'svelte-icons-pack/Icon.svelte';
    import AiOutlineExport from "svelte-icons-pack/ai/AiOutlineExport";
    import AiOutlineSetting from "svelte-icons-pack/ai/AiOutlineSetting";
    import AiOutlineShop from "svelte-icons-pack/ai/AiOutlineShop";
    import AiOutlineTeam from "svelte-icons-pack/ai/AiOutlineTeam";
    import FaSolidCat from "svelte-icons-pack/fa/FaSolidCat";
    import '../app.css';
    import logo from "../images/letter-f.png";

    const side = "left" as const;
</script>

<main>
    <section>
    <div class="fixed h-[3.5rem] max-h-[16vh] flex box-border w-[100%] top-0">
    <nav class="h-full border-y border-solid flex flex-row w-[100%] p-0 bg-white bg-opacity-75 backdrop-blur-xl">
        <div class="flex basis-1/4 justify-center items-center">
            <div class="size-11 flex justify-center items-center">
                <div class="size-7">    
                <Sheet.Root>
                    <Sheet.Trigger>
                        <Avatar.Root class="size-7">
                            <Avatar.Image src="https://github.com/shadcn.png" alt="@shadcn" />
                            <Avatar.Fallback>CN</Avatar.Fallback>
                        </Avatar.Root>
                    </Sheet.Trigger>
                    <Sheet.Content {side}>
                      <div class="pb-4">
                        <div class="size-10">
                            <a href="/profile">
                                <Avatar.Root class="size-10">
                                    <Avatar.Image src="https://github.com/shadcn.png" alt="@shadcn" />
                                    <Avatar.Fallback>CN</Avatar.Fallback>
                                </Avatar.Root>
                            </a>
                        </div>
                        <div class="mt-2">
                            <a href="/profile">
                                <p class="font-bold">Name</p>
                                <p class="text-slate-500">@username</p>
                            </a>
                        </div>
                        <div class="mt-2 flex gap-2 text-sm">
                          <div><a href="/following"><span class="font-bold">0</span><span class="ml-1 text-slate-500">Following</span></a></div>
                          <div><a href="/followers"><span class="font-bold">0</span><span class="ml-1 text-slate-500">Followers</span></a></div>
                        </div>
                      </div>
                      <div class="py-4">
                        <a href="/pet-profile" class="flex flex-row">
                          <div class="flex mr-6">
                            <div class="size-11 flex justify-center items-center">
                              <div class="size-7 ">
                                  <Icon src={FaSolidCat} className='custom-icon'/>
                              </div>
                            </div>
                          </div>
                          <div class="flex items-center"><p class="font-bold text-xl">Pet Profile</p></div>
                        </a>
                      </div>
                      <div class="py-4">
                        <a href="/shop" class="flex flex-row">
                          <div class="flex mr-6">
                            <div class="size-11 flex justify-center items-center">
                              <div class="size-7 ">
                                  <Icon src={AiOutlineShop} className='custom-icon'/>
                              </div>
                            </div>
                          </div>
                          <div class="flex items-center"><p class="font-bold text-xl">Shop</p></div>
                        </a>
                      </div>
                      <div class="py-4">
                        <a href="/communities" class="flex flex-row">
                          <div class="flex mr-6">
                            <div class="size-11 flex justify-center items-center">
                              <div class="size-7 ">
                                  <Icon src={AiOutlineTeam} className='custom-icon'/>
                              </div>
                            </div>
                          </div>
                          <div class="flex items-center"><p class="font-bold text-xl">Communities</p></div>
                        </a>
                      </div>
                      <div class="py-4">
                        <a href="/logout" class="flex flex-row">
                          <div class="flex mr-6">
                            <div class="size-11 flex justify-center items-center">
                              <div class="size-7 ">
                                  <Icon src={AiOutlineExport} className='custom-icon'/>
                              </div>
                            </div>
                          </div>
                          <div class="flex items-center"><p class="font-bold text-xl">Log Out</p></div>
                        </a>
                      </div>
                    </Sheet.Content>
                  </Sheet.Root>
            </div></div>
            
            </div>
        <a href="/" class="flex basis-2/4 justify-center items-center">
            <div class="size-11 flex justify-center items-center">
                <div class="size-7 ">
                    <img src={logo} alt="" class="size-7">
                </div>
            </div>
        </a>
        <a href="/settings" class="flex basis-1/4 justify-center items-center">
            <div class="size-11 flex justify-center items-center">
                <div class="size-5">
                    <Icon src={AiOutlineSetting} size=20/>
                </div>
            </div>
        </a>
    </nav>
</div>
</section>

<section>
    <div class="pt-14 px-4">
    <h1 class="scroll-m-20 text-4xl font-extrabold tracking-tight lg:text-5xl">
      The Joke Tax Chronicles
    </h1>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      Once upon a time, in a far-off land, there was a very lazy king who spent
      all day lounging on his throne. One day, his advisors came to him with a
      problem: the kingdom was running out of money.
    </p>
    <h2
      class="mt-10 scroll-m-20 border-b pb-2 text-3xl font-semibold tracking-tight transition-colors first:mt-0"
    >
      The King's Plan
    </h2>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      The king thought long and hard, and finally came up with{" "}
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#" class="font-medium text-primary underline underline-offset-4">
        a brilliant plan
      </a>
      : he would tax the jokes in the kingdom.
    </p>
    <blockquote class="mt-6 border-l-2 pl-6 italic">
      "After all," he said, "everyone enjoys a good joke, so it's only fair that
      they should pay for the privilege."
    </blockquote>
    <h3 class="mt-8 scroll-m-20 text-2xl font-semibold tracking-tight">
      The Joke Tax
    </h3>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      The king's subjects were not amused. They grumbled and complained, but the
      king was firm:
    </p>
    <ul class="my-6 ml-6 list-disc [&>li]:mt-2">
      <li>1st level of puns: 5 gold coins</li>
      <li>2nd level of jokes: 10 gold coins</li>
      <li>3rd level of one-liners : 20 gold coins</li>
    </ul>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      As a result, people stopped telling jokes, and the kingdom fell into a
      gloom. But there was one person who refused to let the king's foolishness
      get him down: a court jester named Jokester.
    </p>
    <h3 class="mt-8 scroll-m-20 text-2xl font-semibold tracking-tight">
      Jokester's Revolt
    </h3>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      Jokester began sneaking into the castle in the middle of the night and
      leaving jokes all over the place: under the king's pillow, in his soup, even
      in the royal toilet. The king was furious, but he couldn't seem to stop
      Jokester.
    </p>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      And then, one day, the people of the kingdom discovered that the jokes left
      by Jokester were so funny that they couldn't help but laugh. And once they
      started laughing, they couldn't stop.
    </p>
    <h3 class="mt-8 scroll-m-20 text-2xl font-semibold tracking-tight">
      The People's Rebellion
    </h3>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      The people of the kingdom, feeling uplifted by the laughter, started to tell
      jokes and puns again, and soon the entire kingdom was in on the joke.
    </p>
    <div class="my-6 w-full overflow-y-auto">
      <table class="w-full">
        <thead>
          <tr class="m-0 border-t p-0 even:bg-muted">
            <th
              class="border px-4 py-2 text-left font-bold [&[align=center]]:text-center [&[align=right]]:text-right"
            >
              King's Treasury
            </th>
            <th
              class="border px-4 py-2 text-left font-bold [&[align=center]]:text-center [&[align=right]]:text-right"
            >
              People's happiness
            </th>
          </tr>
        </thead>
        <tbody>
          <tr class="m-0 border-t p-0 even:bg-muted">
            <td
              class="border px-4 py-2 text-left [&[align=center]]:text-center [&[align=right]]:text-right"
            >
              Empty
            </td>
            <td
              class="border px-4 py-2 text-left [&[align=center]]:text-center [&[align=right]]:text-right"
            >
              Overflowing
            </td>
          </tr>
          <tr class="m-0 border-t p-0 even:bg-muted">
            <td
              class="border px-4 py-2 text-left [&[align=center]]:text-center [&[align=right]]:text-right"
            >
              Modest
            </td>
            <td
              class="border px-4 py-2 text-left [&[align=center]]:text-center [&[align=right]]:text-right"
            >
              Satisfied
            </td>
          </tr>
          <tr class="m-0 border-t p-0 even:bg-muted">
            <td
              class="border px-4 py-2 text-left [&[align=center]]:text-center [&[align=right]]:text-right"
            >
              Full
            </td>
            <td
              class="border px-4 py-2 text-left [&[align=center]]:text-center [&[align=right]]:text-right"
            >
              Ecstatic
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      The king, seeing how much happier his subjects were, realized the error of
      his ways and repealed the joke tax. Jokester was declared a hero, and the
      kingdom lived happily ever after.
    </p>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      The moral of the story is: never underestimate the power of a good laugh and
      always be careful of bad ideas.
    </p>
  </div>
</section>
</main>
