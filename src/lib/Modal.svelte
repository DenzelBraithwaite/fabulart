<script>
    import Button from '$lib/Button.svelte';
</script>

<div class="backdrop">
    <div class="modal">
        <div class="text-wrapper">
            <h2>Modal title here?</h2>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Labore ad adipisci accusamus atque odit illo temporibus minima! Aspernatur consequatur qui cumque, atque, dolore quod aliquam voluptas repellendus, magnam magni eos.</p>
        </div>
        <Button bgColor="bg-red" textColor="text-white">Close</Button>
    </div>
</div>

<style>
    .backdrop {
        position: relative;
        background-color: #000000ce;
        height: 200px;
    }

    .modal {
        width: 50%;
        margin: 0 auto;
        background-color: #fff;

        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        border-radius: 0.25rem;
    }
</style>