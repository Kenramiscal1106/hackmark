<script lang="ts">
  import Navbar from "../../components/navbar.svelte";
</script>
<Navbar target="/css/introduction" firstPath="/css" links={[
  {link:'/introduction', title:'CSS Introduction'},
  {link:'/howto', title: 'CSS How To'}
]} vertical={true}/>
<svelte:head>
  <title>CSS Introduction</title>
</svelte:head>
<main>
  <h1>CSS Introduction</h1>
  <p>CSS stands for <b>c</b>ascading <b>s</b>tyle <b>s</b>heets</p>
</main>