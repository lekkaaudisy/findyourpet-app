<script lang='ts'>
    import Icon from 'svelte-icons-pack/Icon.svelte';
    import AiOutlineBell from "svelte-icons-pack/ai/AiOutlineBell";
    import AiOutlineHome from "svelte-icons-pack/ai/AiOutlineHome";
    import AiOutlineMail from "svelte-icons-pack/ai/AiOutlineMail";
    import AiOutlineSearch from "svelte-icons-pack/ai/AiOutlineSearch";
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