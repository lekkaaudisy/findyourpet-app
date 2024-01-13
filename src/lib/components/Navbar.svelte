<script lang='ts'>
    import * as Avatar from "$lib/components/ui/avatar";
    import * as Sheet from "$lib/components/ui/sheet";
    import Icon from 'svelte-icons-pack/Icon.svelte';
    import AiOutlineBell from "svelte-icons-pack/ai/AiOutlineBell";
    import AiOutlineExport from "svelte-icons-pack/ai/AiOutlineExport";
    import AiOutlineHome from "svelte-icons-pack/ai/AiOutlineHome";
    import AiOutlineMail from "svelte-icons-pack/ai/AiOutlineMail";
    import AiOutlineSearch from "svelte-icons-pack/ai/AiOutlineSearch";
    import AiOutlineSetting from "svelte-icons-pack/ai/AiOutlineSetting";
    import AiOutlineShop from "svelte-icons-pack/ai/AiOutlineShop";
    import AiOutlineTeam from "svelte-icons-pack/ai/AiOutlineTeam";
    import FaSolidCat from "svelte-icons-pack/fa/FaSolidCat";
    import '../../app.css';
    import logo from "../../images/letter-f.png";

    const side = "left" as const;
</script>

<div class="fixed h-[3.5rem] max-h-[16vh] flex box-border w-[100%] bottom-0">
    <nav class="h-full border-y border-solid flex flex-row w-[100%] p-0 bg-white cursor-pointer">
        <a href="/" class="flex basis-1/4 justify-center items-center">
            <div class="size-11 flex justify-center items-center">
                <div class="size-7 ">
                    <Icon src={AiOutlineHome} className='custom-icon'/>
                </div>
            </div>
        </a>
        <a href="/search" class="flex basis-1/4 justify-center items-center">
            <div class="size-11 flex justify-center items-center">
                <div class="size-7 ">
                    <Icon src={AiOutlineSearch} className='custom-icon'/>
                </div>
            </div>
        </a>
        <a href="/notifications" class="flex basis-1/4 justify-center items-center">
            <div class="size-11 flex justify-center items-center">
                <div class="size-7 ">
                    <Icon src={AiOutlineBell} className='custom-icon'/>
                </div>
            </div>
        </a>
        <a href="/messages" class="flex basis-1/4 justify-center items-center">
            <div class="size-11 flex justify-center items-center">
                <div class="size-7 ">
                    <Icon src={AiOutlineMail} className='custom-icon'/>
                </div>
            </div>
        </a>
    </nav>
</div>
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
                        <a href="/login" class="flex flex-row">
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
            </div>
          </div>
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
