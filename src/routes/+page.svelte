<script>
  import { person } from "/src/lib/data.js";
</script>

<main>
  <section>
    {#each person as person}
      <article class="card">
        <img
          src="/{person.image}"
          width="300px"
          height="300px"
          alt="Linkedin photo"
        />
        <a href={person.url} target="_blank">
          <h1>{person.name}</h1>
          <p>{person.title}</p>
          <p>{person.url}</p>
          <p>{person.email}</p>
        </a>
      </article>
    {/each}
  </section>
</main>

<style>
  section {
    padding: 10rem;
    display: flex;
    justify-content: center;
  }
  article {
    border: 1px solid black;
    background-color: white;
    border-radius: 3rem;
    padding: 5rem;
    width: 35%;
    text-align: center;
  }
  a {
    color: black;
    text-decoration: none;
  }

  article:hover {
    background-color: lightgrey;
    box-shadow: black;
  }
</style>
