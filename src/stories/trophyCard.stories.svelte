<script module>
  import { defineMeta } from '@storybook/addon-svelte-csf';
  import TrophyCard from '$lib/components/TrophyCard/TrophyCard.svelte';

  // More on how to set up stories at: https://storybook.js.org/docs/writing-stories
  const { Story } = defineMeta({
    title: 'Example/Trophy Card',
    component: TrophyCard,
    tags: ['autodocs'],
    argTypes: {
      rarity: {
        control: { type: 'select' },
        options: ['bronze', 'silver', 'gold', 'platinum']
      }
    }
  });
</script>

<!-- More on writing stories with args: https://storybook.js.org/docs/writing-stories/args -->
<Story name="Primary" args={{ desc: "Do the thing", name: "Did the thing", rarity: "bronze" }} />

