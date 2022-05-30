<script>
	export let id;
	export let paliname;
	export let engname;
	export let meaning;
	export let hiLiteSel;
	
	const lessonLinks = ["Introduction", "English", "Pali", "Compare", "Flashcards"];
</script>


<header>
	<p class="namo-tassa">
		Namo tassa bhagavato arahato sammāsambuddhassa
	</p>
	<h1 title={meaning}>Lesson {id}<br />
			<strong>{paliname}</strong></h1>
	<h2>{engname}</h2>	
	
	<nav>
		{#each lessonLinks as linkName, i}
			<button title={linkName}	
							data-index={i} 
							class:highlight={linkName === hiLiteSel}
							on:click>{linkName}</button>
		{/each}
	</nav>
</header>	


<style>
	header {
		text-align: center;
		padding: 1rem 0.5rem;
		background-color: #dcd3c0;
	}

	header p.pali {
		text-align: center;
	}
	
	
	nav {
		margin: 10px 0 0 0 ;
		padding: 0;
	}
	
	.highlight {
		background: #1372BA;
	}
</style>