<script lang="ts">
  interface linkFormat {
    link:string,
    title:string
  }
  export let target: string = '';
  export let vertical:boolean = false;
  export let firstPath: string = '';
  export let links:linkFormat[] = [
    {link:'/', title:'HOME'},
    {link:'/html',title:'HTML'},
    {link:'/css',title:'CSS'},
    {link:"/markdown", title:'Markdown'}
  ]
</script>
<nav class={vertical ? 'sidebar' : 'vertical'}>
    {#each links as link}
      <a href={`${firstPath}${link.link}`} class:active={target === link.link}>{link.title}</a>
    {/each}
 
</nav>
<style lang="scss" >
  @import '../variables';
  nav {
  display: flex;
  background: $nav_bg;
  &.sidebar {
    display: grid;
  }
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