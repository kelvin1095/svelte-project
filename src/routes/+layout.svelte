<script lang="ts">
  import Header from "./header.svelte";
  import Footer from "./footer.svelte";
  import Navigate from "./navigate.svelte";
</script>

<div id="root">
  <div id="header"><Header /></div>
  <div id="mainContent">
    <div id="leftColumn">
      <Navigate />
    </div>
    <div id="mainColumn">
      <slot />
    </div>
    <div id="rightColumn"></div>
  </div>
  <div id="footer">
    <Footer />
  </div>
</div>

<style lang="sass">
  @import url("https://fonts.googleapis.com/css2?family=Cormorant:wght@500&family=Ysabeau:wght@500&display=swap")

  :global(body)
    font-family: "Ysabeau"
    padding: 0
    margin: 0  
    
  :global(h1)
    font-weight: normal
    padding: 0
    margin: 0

  :global(ul)
    list-style: none
    padding: 0

  :global(a)
    text-decoration: none
    color: inherit

  #root
    display: flex
    flex-direction: column
    min-height: 100vh

  #mainContent
    width: 1024px
    flex-grow: 1
    display: flex
    margin: 0.5rem auto

    #leftColumn
      flex-grow: 1
      width: 5rem

    #mainColumn
      flex-grow: 1
      width: 66.666%

    #rightColumn
      flex-grow: 1
      width: 5rem
</style>
