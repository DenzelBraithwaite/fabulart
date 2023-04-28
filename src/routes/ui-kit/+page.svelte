<script>
    import Button from '$lib/Button.svelte';
    import Navbar from '$lib/Navbar.svelte';
</script>

<a href="/" class="back">Back</a>

<p>These are to show what the UI components will look like, we can still tweak them before using them in the application</p>
<div class="container">
    <main>
        <h1 class="btn-title">Buttons</h1>
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

            <div class="wrapper">
                <h2>Blue</h2>
                <Button textColor="text-white" bgColor="bg-blue">Click me</Button>
                <Button textColor="text-blue" border={true} borderColor="border-blue"/>
                <Button shape="round" textColor="text-white" bgColor="bg-blue">Click me</Button>
                <Button shape="round" textColor="text-blue" border={true} borderColor="border-blue"/>
            </div>

            <div class="wrapper">
                <h2>Red</h2>
                <Button textColor="text-white" bgColor="bg-red">Click me</Button>
                <Button textColor="text-red" border={true} borderColor="border-red"/>
                <Button shape="round" textColor="text-white" bgColor="bg-red">Click me</Button>
                <Button shape="round" textColor="text-red" border={true} borderColor="border-red"/>
            </div>

            <div class="wrapper">
                <h2>Green</h2>
                <Button textColor="text-white" bgColor="bg-green">Click me</Button>
                <Button textColor="text-green" border={true} borderColor="border-green"/>
                <Button shape="round" textColor="text-white" bgColor="bg-green">Click me</Button>
                <Button shape="round" textColor="text-green" border={true} borderColor="border-green"/>
            </div>
        </section>

        <h1 class="nav-title">Navbars</h1>
        <section>
            <Navbar backgroundColor="bg-peach"/>
            <Navbar backgroundColor="bg-yellow"/>
            <Navbar backgroundColor="bg-blue"/>
            <Navbar backgroundColor="bg-red"/>
            <Navbar backgroundColor="bg-green"/>
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
        border-radius: 100px;
    }

    .nav-title {
        width: 100%;
        background-color: #bebebe;
        text-align: center;
    }

    h2 {
        color: #444;
    }

    .back {
        display: block;
        margin-bottom: 5rem;
    }
</style>