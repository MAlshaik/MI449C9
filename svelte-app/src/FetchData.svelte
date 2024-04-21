<script>
    let product = null;

    fetch('https://dummyjson.com/products/1')
        .then(response => response.json())
        .then(json => product = json);
</script>

{#if product}
<main style="display: flex; justify-content: center; align-items: center; height: 100vh;">
    <div>
        <h1>{product.title}</h1>
        <p>{product.description}</p>
        <p>Price: {product.price}</p>
        <p>Discount: {product.discountPercentage}%</p>
        <p>Rating: {product.rating}</p>
        <img src={product.thumbnail} alt={product.title} />
    </div>
</main>
{/if}

