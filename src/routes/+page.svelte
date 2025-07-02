<script lang="ts">
    import Header from "./Header.svelte";

    let name = $state( "Scott");

    let status: 'OPEN' | 'CLOSED' = $state('OPEN')
    function onclick() {
        status = status === 'OPEN' ? 'CLOSED' : 'OPEN';
    }
    // function toggle() {
    //     status = status === 'OPEN' ? 'CLOSED' : 'OPEN';
    // }
</script>

<Header {name} />

<input type="text" bind:value={name}/>

<p>The store is now {status}</p>

<button onclick = {()=>{
    status = status === 'OPEN' ? 'CLOSED' : 'OPEN';
}}>Toggle Status</button>
<!-- <button {onclick}>Toggle Status</button> -->