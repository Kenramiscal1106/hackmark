<script lang="ts">
import { tab } from "./stores";
  let activeTab : string;
  tab.subscribe(current => {
    activeTab = current
  }
  )

  interface linkFormat {
    link:string,
    title:string
  }
  let links:linkFormat[] = [
    {link:'/', title:'HOME'},
    {link:'/html',title:'HTML'},
    {link:'/css',title:'CSS'},
    {link:"/markdown", title:'Markdown'}
  ]
</script>
<main>
  <nav class='navtop'>
      {#each links as link}
        <a href={link.link} class:active={activeTab == link.link}>{link.title}</a>
      {/each}
   
  </nav>
  <slot></slot>
</main>
<style lang="scss" >
  @import '../styles';
  @import '../variables';
  nav {
  display: flex;
  background: $nav_bg;
  > a {
    display: block;
    color:$nav_text; 
    padding: 0.75rem 1rem;
    &:hover {
      background: $hover_nav_bg;
    }
    &.active {
      background: $nav_active;
    }
  }
}
</style>