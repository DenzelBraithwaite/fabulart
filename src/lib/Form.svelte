<script>
    import Layout from '../routes/layout.svelte';
    export let action = '/';
</script>

<!-- The svelte:component is to apply global css from the src/routes/__layout.svelte file -->
<svelte:component this={Layout}>
<form action="{action}">
    <h2 class="form-title">Create your story!</h2>
    <div class="form-control">
        <input type="text" id="title" name="title" placeholder="Enter your story title here">
    </div>
    <div class="form-control">
        <textarea name="img-description" id="img-description" placeholder="Describe the image you would like to see! Example: 'friends playing soccer outiside on a sunny day!'"></textarea>
    </div>
    <button type="submit">Create</button>
</form>
</svelte:component>

<style>
    form {
        position: relative;
        box-shadow: 0 4px 8px #0000002c;
        width: 50%;
        margin: 0 auto;
        text-align: center;
        background-color: green;
        background-color: #D98684;
        padding: 2rem 1rem;
        border-radius: 1.5rem;
    }

    .form-control {
        position: relative;
        width: 100%;
        margin: 2rem 0;
        background-color: yellow;
    }

    .form-title {
        color: #fff;
    }

    input {
        outline: none;
        border: none;
        width: 90%;
        background-color: red;
    }

    textarea {
        width: 90%;
    }

    button {
        border: none;
        display: inline-block;
        text-decoration: none;
        text-align: center;
        padding: 0.5rem 1rem;
        border-radius: 100px;
    }

    button:hover,
    button:active {
        cursor: pointer;
    }
</style>