<script lang="ts">
  import { page } from "$app/stores";
  import { goto } from "$app/navigation";
  import Section from "../section.svelte";
  import Toggle from "../toggle.svelte";
  import PricingBoxes from "./pricing-boxes.svelte";
  import type { Pricing } from "$lib/types/pricing.type";

  export let pricingPlans: Pricing[];

  let toggled: boolean = false;

  const handleChange = (e: Event) => {
    const slug = $page.path.split("/")[1];
    toggled = (<HTMLInputElement>e.target).checked;
    setTimeout(() => {
      if (slug === "pricing") {
        if (toggled) {
          goto("/self-hosted");
        } else {
          goto("/pricing");
        }
      } else {
        if (toggled) {
          goto("/pricing");
        } else {
          goto("/self-hosted");
        }
      }
    }, 400);
  };
</script>

<Section>
  <h1 class="text-center">Plans and pricing</h1>
  <Toggle
    class="mb-xx-small"
    labelLeft="SaaS"
    labelRight="Self-hosted"
    on:change={handleChange}
    isInversed={$page.path.includes("self-hosted")}
  />
  <PricingBoxes {pricingPlans} />
  <p class="mt-micro text-center">
    Can’t find the answer here? <a href="/contact/sales">Contact sales</a>
  </p>
</Section>
