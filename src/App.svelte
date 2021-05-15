<script>
  import TextInput from "./components/TextInput.svelte";
  export let name;
</script>

<main>
  <h1>Hello {name}!</h1>
  <TextInput id="name" type="text" label="Name"/>
  <TextInput id="email" type="email" label="email"/>
  <TextInput id="contactno" type="number" label="contactno"/>
  <TextInput id="password" type="password" label="password"/>
  <TextInput id="date" type="date" label="date"/>
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

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
