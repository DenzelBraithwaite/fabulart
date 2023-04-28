<script>
    import Button from '$lib/Button.svelte'
</script>

<a href="/" class="back">Back</a>

<div class="container">
    <main>
        <h1 class="btn-title">Buttons</h1>
        <!-- Square buttons -->
        <section>
            <div class="wrapper">
                <h2>Peach</h2>
                <Button textColor="text-white" bgColor="bg-peach">Click me</Button>
                <Button textColor="text-peach" border={true} borderColor="border-peach"/>
                <Button shape="round" textColor="text-white" bgColor="bg-peach">Click me</Button>
                <Button shape="round" textColor="text-peach" border={true} borderColor="border-peach"/>
            </div>
            
            <div class="wrapper">
                <h2>Yellow</h2>
                <Button textColor="text-white" bgColor="bg-yellow">Click me</Button>
                <Button textColor="text-yellow" border={true} borderColor="border-yellow"/>
                <Button shape="round" textColor="text-white" bgColor="bg-yellow">Click me</Button>
                <Button shape="round" textColor="text-yellow" border={true} borderColor="border-yellow"/>
            </div>
        </section>

        <!-- Round buttons -->
        <section>
            <Button shape="round" textColor="text-white" bgColor="bg-peach">Click me</Button>
            <Button shape="round" textColor="text-black" border={true} />
        </section>
    </main>
</div>

<style>
    .container {
        width: 90%;
        margin: 0 auto;
        box-shadow: 0 2px 8px #0000001e;
        border-radius: 50px 50px 0 0;
        padding: 1rem;
    }

    section {
        margin-bottom: 2rem;
    }

    .wrapper {
        margin-bottom: 5rem;
    }

    .btn-title {
        text-align: center;
        background-color: #bebebe;
        padding: 0.5rem 1rem;
        width: 50%;
        margin: 0 auto;

    }

    .back {
        display: block;
        margin-bottom: 5rem;
    }
</style>