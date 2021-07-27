<script>
 export let id;
  export let location;
  // global store

  import products from "../stores/defaultProducts";
  import Loading from "../components/Loading.svelte";
  import { link } from "svelte-routing";

  $: product = $products.find(item => item.id === parseInt(id));
</script>
<svelte:head>
  <title>{!product ? 'Italia\'s': product.title}</title>
</svelte:head>
{#if !product}
  <Loading />
{:else}
<section class="single-product">
  <!-- back to products -->
  <a href="/products" use:link class="btn btn-primary">volver a productos</a>
  <!-- single product container -->
  <div class="single-product-container">
    <article class="single-product-image">
      <img src={product.image} alt={product.title}>
    </article>
    <article>
      <h1>{product.title}</h1>
      <h2>{product.price}</h2>
      <button class="btn btn-primary btn-block" on:click={()=>{console.log("hello")}}>agregar al carrito</button>
    </article>
  </div>
</section>
{/if}
