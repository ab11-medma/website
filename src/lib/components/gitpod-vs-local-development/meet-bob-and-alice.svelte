<script>
  import { intros } from "$lib/contents/gitpod-vs-local-development";

  import Section from "../section.svelte";
  import ComparisonGraphic from "./comparison-graphic.svelte";
  import ComparisonTable from "./comparison-table.svelte";
</script>

<style lang="postcss">
  .intros {
    max-width: 820px;
  }
  .intros :global(ul) {
    @apply pl-small list-disc;
  }
</style>

<Section>
  <div class="text-center">
    <h2>Meet Bob and Alice</h2>
    <p class="text-large">
      Let’s have a closer look on how desktop and cloud development
      differentiate.
    </p>
  </div>
  <div
    class="intros flex flex-col lg:flex-row items-center lg:items-start mx-auto justify-between mt-small lg:mt-x-large lg:space-x-medium space-y-x-large lg:space-y-0"
  >
    {#each intros as { image, name, works, workflow, isHighlighted }}
      <div class="max-w-sm">
        <img src={image} alt={name} class="h-56 w-56 mx-auto" />
        <div class="text-center">
          <h3 class="h4 mt-micro mb-macro">
            {name}
          </h3>
          <p>{works}</p>
        </div>
        <div
          class="bg-white px-x-small py-xx-small mt-x-small rounded-2xl shadow-normal"
          class:shadow-brand={isHighlighted}
        >
          {@html workflow}
        </div>
      </div>
    {/each}
  </div>

  <ComparisonTable />

  <ComparisonGraphic />
</Section>
