<script lang="ts">
    import Block from './block.svelte';

    let count = $state(0)

    const towerglass_pkg = {
        name: 'Towerglass',
        desc: 'Anxiety inducing platformer for GMTK',
        num: 1,
    }

    const blendobar_pkg = {
        name: 'Blend O\' Bar',
        desc: 'Exploration cooking game',
        num: 13,
    }

    const stockstriker_pkg = {
        name: 'Stock Strikers',
        desc: 'Financial Rouglite Chaos',
        num: 11,
    }

    function increment() {
        count += 1;
    }
</script>

<h1>Welcome to My Portfolio!</h1>

<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<button onclick={increment}>
    CLICK ME {count}
</button>

{#if count % 3 == 0}
    <p>{count} is divisible by 3</p>
{:else}
    <p>{count} is not divisible by 3</p>
{/if}

<Block {...towerglass_pkg}/>
<Block {...blendobar_pkg}/>
<Block {...stockstriker_pkg}/>