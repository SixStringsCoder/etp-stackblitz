<script context="module">
	export const prerender = true;
</script>

<script>
  import { suttaData } from './exploring-the-path/data.js'

  const url = "https://stackblitz.com/edit/sveltejs-kit-template-default-gsbsub/exploring-the-path/"

</script>

<svelte:head>
	<title>Exploring the Path</title>
	<meta name="description" content="Svelte ETP app" />
</svelte:head>

<h1>Exploring the Path</h1>
<h2>Overview of the lessons</h2>
<section id="lesson-cards">
  {#each suttaData as suttaObj, i}
    <div class="card">
      <h3>{`${suttaObj.id} ${suttaObj.paliname}`}</h3>
      <h3>({`${suttaObj.engname}`})</h3>
      <p>{suttaObj.blurb}</p>
      <a href={`${url}lesson-${suttaObj.id}`}><button id={`${i}`}>Go to Lesson</button></a>
    </div>
  {/each}
</section>

<style>
section#lesson-cards {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}

.card {
	width: 80%;
	margin: 10px 0;
	box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 65%);
	padding: 16px;
	text-align: center;
	background-color: hsl(39, 37%, 85%);
	border-radius: 15px;
}

h3 {
    margin: 5px 0;
}

p {
	margin: 8px;
}
</style>
