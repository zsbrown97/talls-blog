<script lang="ts">
  import bronze from '$lib/components/TrophyCard/images/bronze.png';
  import gold from '$lib/components/TrophyCard/images/gold.png';
  import plat from '$lib/components/TrophyCard/images/plat.png';
  import silver from '$lib/components/TrophyCard/images/silver.png';

	type Props = {
    desc: string
		name: string
    rarity: 'bronze' | 'silver' | 'gold' | 'platinum'
		
	}

	let { desc, name, rarity }: Props = $props()
</script>

<div class="card">
  <div class="rarity">
    {#if rarity == 'bronze'}
      <img src={bronze} />
    {:else if rarity == 'silver'}
      <img src={silver} />
    {:else if rarity == 'gold'}
      <img src={gold} />
    {:else if rarity == 'platinum'}
      <img src={plat} />
    {/if}
  </div>
  <div class="trophyDetails">
    <h2 class="trophyName">{name}</h2>
    <p>{desc}</p>
  </div>
  
</div>

<style>
  .card {
    align-items: center;
    border-radius: 0.5rem;
    box-shadow: 0 0.25rem 0.5rem 0 rgba(0,0,0,0.2);
    display: flex;
    flex-direction: row;
    justify-content: center;
    min-width: 20%;
    max-width: 70%;
    
  }

  .rarity {
    display: flex;
    align-content: center;
    padding: 0 1rem;
  }

  .trophyName {
    display: flex;
    font-size: 1.5rem;
    font-weight: bold;
  }
  

</style>