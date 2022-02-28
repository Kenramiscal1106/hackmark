<script lang="ts">
  import Navbar from "../../components/navbar.svelte";
</script>
<svelte:head>
  <title>Markdown</title>
</svelte:head>
<Navbar vertical={false} target="/markdown"/>
<Navbar links={[
  {title:'Introduction',link:'/introduction'},
  {title:'How To',link:'/how-to'},
  {title:'Headings',link:'/headings'},
  {title:'paragraphs and Styles',link:'/paragraph-and-styles'}
]} firstPath="/markdown" vertical={true}/>
<main>
  <h1>Markdown</h1>
  <p>Is a markup language used for documentations, messaging and READMEs.</p>
  <a href="/markdown/introduction">Start learning markdown now</a>
</main>