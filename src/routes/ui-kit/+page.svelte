<script>
    import Button from '$lib/Button.svelte';
    import Navbar from '$lib/Navbar.svelte';
    import Form from '$lib/Form.svelte';
    import Modal from '$lib/Modal.svelte';
</script>

<svelte:head>
<title>Fabulart | UI kit</title>
</svelte:head>


<p class="message"><mark>⚠️These are to show what the UI components will look like, we can still tweak them before using them in the application</mark></p>
<div class="container">
    <main>
        <Button url="/" bgColor="bg-danger" textColor="text-white">Back</Button>
        <h1 class="btn-title">Buttons</h1>
        <section>
            <div class="wrapper">
                <h2>pink</h2>
                <Button textColor="text-white" bgColor="bg-pink">Click me</Button>
                <Button textColor="text-pink" border={true} borderColor="border-pink"/>
                <Button shape="round" textColor="text-white" bgColor="bg-pink">Click me</Button>
                <Button shape="round" textColor="text-pink" border={true} borderColor="border-pink"/>
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

            <div class="wrapper">
                <h2>Purple</h2>
                <Button textColor="text-white" bgColor="bg-purple">Click me</Button>
                <Button textColor="text-purple" border={true} borderColor="border-purple"/>
                <Button shape="round" textColor="text-white" bgColor="bg-purple">Click me</Button>
                <Button shape="round" textColor="text-purple" border={true} borderColor="border-purple"/>
            </div>
        </section>

        <h1 class="nav-title">Navbars</h1>
        <section>
            <h2>Pink</h2>
            <Navbar logoCentered={true} backgroundColor="bg-pink"/>
            <Navbar backgroundColor="bg-pink"/>

            <h2>Yellow</h2>
            <Navbar logoCentered={true} backgroundColor="bg-yellow"/>
            <Navbar backgroundColor="bg-yellow"/>

            <h2>Blue</h2>
            <Navbar logoCentered={true} backgroundColor="bg-blue"/>
            <Navbar backgroundColor="bg-blue"/>

            <h2>Red</h2>
            <Navbar logoCentered={true} backgroundColor="bg-red"/>
            <Navbar backgroundColor="bg-red"/>

            <h2>Green</h2>
            <Navbar logoCentered={true} backgroundColor="bg-green"/>
            <Navbar backgroundColor="bg-green"/>

            <h2>Purple</h2>
            <Navbar logoCentered={true} backgroundColor="bg-purple"/>
            <Navbar backgroundColor="bg-purple"/>
        </section>

        <h1 class="form-title">Forms</h1>
        <section>
            <Form bgColor="bg-pink" />
            <Form bgColor="bg-pink" newStory={false}/>
            <Form bgColor="bg-yellow"/>
            <Form bgColor="bg-yellow" newStory={false}/>
        </section>

        
        <div class="backdrop">
            <h1 class="modal-title">Modals</h1>
        </div>
        <section>
            <Modal></Modal>
            <Modal></Modal>
        </section>
    <Button url="/" bgColor="bg-danger" textColor="text-white">Back</Button>
    </main>
</div>

<style>
    .container {
        width: 90%;
        margin: 0 auto;
        box-shadow: 0 2px 8px #0000001e;
        border-radius: 0.5rem;
        padding: 1rem;
    }

    section {
        margin-bottom: 2rem;
    }

    .wrapper {
        margin-bottom: 5rem;
    }

    .message {
        text-align: center;
        margin: 5rem auto 1rem;
    }

    .btn-title {
        text-align: center;
        background-color: #bebebe;
        padding: 0.5rem 1rem;
        width: 30%;
        margin: 5rem auto 3rem;
        border-radius: 100px;
    }

    .nav-title {
        width: 100%;
        padding: 1rem 0;
        background-color: #bebebe;
        text-align: center;
        margin: 10rem auto 3rem;
    }

    .form-title {
        text-align: center;
        margin: 3rem auto;
        background-color: #bebebe;
        width: 20%;
        padding: 1rem 0 5rem 0;
        border-radius: 1rem;
        margin: 10rem auto 3rem;
    }

    .modal-title {
        text-align: center;
        background-color: #fff;
        padding: 2rem;
        border-radius: 0.5rem;

        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .backdrop {
        position: relative;
        width: 50%;
        height: 200px;
        background-color: #bebebe;
        margin: 10rem auto 3rem;
    }
</style>