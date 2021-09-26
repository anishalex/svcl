<script>
    export let labeltxt;
    export let fieldid;
    export let inptype;
    export let placeholder;
</script>

<style>
    .content {
      display: grid;
      grid-template-columns: 20% 80%;
      grid-column-gap: 10px;
    }
</style>

<div class="w-full overflow-hidden">    
        <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for={fieldid}>
        {labeltxt}
        </label>
        <input class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white" id={fieldid} type={inptype} placeholder={placeholder}>      
</div>   