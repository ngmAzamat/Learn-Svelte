<script>
    import Hello from "./hello.svelte";
    let name = 'louis';
</script>
<h1>hello, {name}!</h1>
<style>
h1 {
    color: blue;
}
</style>
<Hello></Hello>;