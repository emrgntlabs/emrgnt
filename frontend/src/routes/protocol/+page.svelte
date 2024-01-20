<script>
    import Editor from '@tinymce/tinymce-svelte';

    let tinymceApiKey = import.meta.env.VITE_TINY_MCE_API_KEY;
    let tinymceConf = {
        height:"calc(100vh - 32px)",
        skin:"borderless"
    };

</script>
    
<div class="pl-72 h-dvh">
    <div class="flex flex-col">
        <div class="h-8 pt-2">
            <h1 class="pl-3 text-lg font-semibold">Sample Project</h1>
        </div>
        <div class="grow">
            <Editor
            apiKey={ tinymceApiKey }
            conf={ tinymceConf }
        />
        </div>
        
    </div>
</div>

