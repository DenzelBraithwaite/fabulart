<script>
    import Button from '$lib/Button.svelte'
</script>

<a href="/" class="back">Back</a>

<h1>Buttons</h1>
<Button bgColor="bg-cyan">Click me</Button>
<Button textColor="text-black" border={true} />

<style>
    h1 {
        text-align: center;
    }

    .back {
        display: block;
        margin-bottom: 5rem;
    }
</style>