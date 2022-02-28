<script lang="ts">
  interface linkFormat {
    link:string,
    title:string
  }
  export let vertical:boolean = true;
  export let extraLinks: linkFormat[] = [];
  export let firstPath: string = '';
  let linksAll:linkFormat[] = [
    {link:'/html',title:'HTML'},
    {link:'/css',title:'CSS'},
    {link:"/markdown", title:'Markdown'},
    {link:'/', title:'HOME'}
  ]
</script>
<nav class={vertical ? 'sidebar' : 'vertical'}>
  <div>
    {#each linksAll as link}
      <a href={link.link}>{link.title}</a>
    {/each}
  </div>
  {#if extraLinks.length !== 0}
    <div>
      {#each extraLinks as link}
        <a href={`${firstPath}${link.link}`}>{link.title}</a>
      {/each}
    </div>
  {/if}
 
</nav>
<style lang="scss" >
  @import './navbar';
  .sidebar a {
  display: block;
  }
  .sidebar {
    display: flex;
  }
  .vertical > div {
    display: flex;
  }
</style>