<script lang="ts">
let {name}:{name:string} = $props()
</script>

<h1>Hello from {name }</h1>
<h2>{name.replaceAll('t', 'x')}</h2>


<style>
h1 {
    color: blue;
    font-size: 2em;
    text-align: center;
}
</style>