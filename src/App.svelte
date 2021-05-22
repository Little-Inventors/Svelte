<script>
    import Card from "./Card.svelte";
    let name = "";
    let image = "";
    let descrption = "";
    let done = true;

    $: done =
        name.trim().length === 0 ||
        image.trim().length === 0 ||
        descrption.trim().length === 0
            ? true
            : false;
</script>

<main>
    <div>
        <label for="name"> Name </label>
        <input type="text" bind:value={name} />
        <label for="image"> Image </label>
        <input type="text" bind:value={image} />
        <label for="description"> descrption </label>
        <input type="text" bind:value={descrption} />
        <br />
        <button disabled={done}>Submit</button>
    </div>
    <Card userName={name} userImage={image} userDescp={descrption} />
</main>

<style>
    main {
        text-align: center;
        padding: 1em;
        max-width: 240px;
        margin: 0 auto;
    }
    h1 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 4em;
        font-weight: 100;
    }
    form {
        width: 30rem;
        max-width: 100%;
    }
    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }
</style>
