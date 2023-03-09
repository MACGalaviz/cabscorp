<script>
    import { onMount } from "svelte";
    const endpoint = "http://localhost:3000/";
    let object = { data: ""}

    onMount(async function () {
        const response = await fetch(endpoint);
        const data = await response.json();
        object = data
    });
    
</script>
<h1>{object.data}</h1>