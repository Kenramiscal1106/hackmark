<script lang="ts">
  import Navbar from "../../components/navbar.svelte";
import { tab } from "../stores";
  tab.set('/css')
</script>
<svelte:head>
  <title>CSS</title>
</svelte:head>
<Navbar links={[
  {link:'/css/introduction', title:'CSS Introduction'}
]}/>
<main>
  <h1>Home</h1>
</main>