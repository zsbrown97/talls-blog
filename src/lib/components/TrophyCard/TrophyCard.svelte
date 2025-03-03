<script lang="ts">
	type Props = {
    desc: string
		name: string
    rarity: 'bronze' | 'silver' | 'gold' | 'platinum'
		
	}

	let { desc, name, rarity }: Props = $props()
</script>

<div class="card">
  <div class="rarity">
    {rarity}
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
    max-width: 60%
    
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