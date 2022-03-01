<script>
import Layout from "../../components/layout.svelte";
import Navbar from "../../components/navbar.svelte";

  
</script>
<Layout>
  <Navbar slot="sidebar" links={[
    {link:'/html', title: 'HTML'}, 
    {link:'/css',title: 'CSS'},
    {link:'/markdown',title:"markdown"}
  ]} vertical={true}/>
  <main slot="content">
    user
  </main>

</Layout>