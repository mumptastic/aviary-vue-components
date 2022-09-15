<template>
    <footer aria-label="footer">
        <slot name="Footernav"></slot>
    </footer>  
</template>
    
<script>
    export default {
        name: 'AviaryFooter',
        props: { 
        }
    }
</script>
    
    <!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

footer {
        top: 100vh;
        position: sticky;
        padding: 0 calc(1.5rem * 0.5);
        background: #3c0000;
        color: #fff;


        nav > ul {
          list-style: none;
          padding: 0;

          display: flex;
          flex-wrap: wrap;
          justify-content: center;
          align-items:center;
          min-height: 50px;

        }

        nav > ul > li {
          padding: 10px;
        }

        nav > ul > li > a {
          color: var(--white);
          display: inline-block;
          text-decoration: none;
          white-space: nowrap;
        }
      }
</style>