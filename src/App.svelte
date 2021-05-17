<script>
  let firstName = "Irene";
  let secondName = "Anna";
  let fullName = "";
  let color = "red";

  $: fullName = `${firstName} ${secondName}`;
  $: {
    console.log(color);
    console.log(fullName);
  }
</script>

<main>
  <p>{fullName} -- {color}</p>
  <input bind:value={firstName} />
  <input bind:value={secondName} />

  <!-- <input on:input={handleInput} value={color}/> -->

  <input bind:value={color} />
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
