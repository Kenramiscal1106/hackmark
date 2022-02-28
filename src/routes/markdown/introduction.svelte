<script lang="ts">
  import Navbar from "../../components/navbar.svelte";
</script>
<svelte:head>
  <title>Markdown introduction</title>
</svelte:head>
<Navbar extraLinks={[
  {title:'Introduction',link:'/introduction'},
  {title:'How To',link:'/how-to'},
  {title:'Headings',link:'/headings'},
  {title:'paragraphs and Styles',link:'/paragraph-and-styles'}
]} firstPath="/markdown"/>
<main>
  <h1>Markdown</h1>
  <p>Markdown has a declarative syntax</p>
</main>