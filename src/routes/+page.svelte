<script lang="ts">
    import Header from "./Header.svelte";

    let name = $state( "Scott");

    let status: 'OPEN' | 'CLOSED' = $state('OPEN')
    function onclick() {
        status = status === 'OPEN' ? 'CLOSED' : 'OPEN';
    }
    let full_name = $derived(name + ' ' + 'Harrison');

    // function toggle() {
    //     status = status === 'OPEN' ? 'CLOSED' : 'OPEN';
    // }
</script>

<Header {name} />

<h2>{full_name}</h2>

<input type="text" bind:value={name}/>

<p>The store is now {status}</p>

<button onclick = {()=>{
    status = status === 'OPEN' ? 'CLOSED' : 'OPEN';
}}>Toggle Status</button>
<!-- <button {onclick}>Toggle Status</button> -->