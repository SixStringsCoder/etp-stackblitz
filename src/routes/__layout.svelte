<script>
  import '../styles/global.css';
</script>

<svelte:head>
  <link href="https://pagecdn.io/lib/normalize/8.0.1/normalize.min.css" rel="stylesheet" crossorigin="anonymous"  >
</svelte:head>


<!-- page content -->
<slot></slot>

<footer>
  <p>&copy; Klaus Nothnagel 2022</p>
</footer>

<style>


/* Footer */
footer {
  /* position: fixed;
  left: 0;
  bottom: 0; */
  margin: 0;
  width: 100%;
  
  background-color: rgb(58, 56, 56);
  color: white;
}

footer p {
  margin: 0;
  padding: 10px;
  text-align: center;
}
</style>