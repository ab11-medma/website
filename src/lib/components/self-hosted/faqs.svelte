<script lang="ts">
  import Section from "../section.svelte";
  import Faqs from "../faqs/faqs.svelte";
  import Faq from "../faqs/faq.svelte";
</script>

<style lang="scss">
  h2 {
    text-align: center;
  }
</style>

<Section>
  <Faqs>
    <h2 class="h1">FAQs</h2>
    <Faq title="Can I create a team plan?">
      <p>
        Of course! You can use Gitpod Self-Hosted Community on your own
        infrastructure for free for unlimited users. If you'd like to try
        additional features like unlimited prebuilds, shared workspaces,
        snapshots and an admin dashboard, the Free tier is available without a
        license for the first 10 users. You can upgrade to to the Professional
        Plan at any time. Simply update your existing instance with a license
        key. Currently, Self-hosted Gitpod licenses can currently only be
        purchased through contacting sales. Please <a href="/enterprise-license"
          >request a license</a
        >
        key or <a href="/contact/sales">Get in touch</a> if you have any questions.
      </p>
    </Faq>
    <Faq title="Can I add more users to my plan at any time?">
      <p>
        Yes, you can add as many users as you like to your plan at any time.
      </p>
    </Faq>
    <Faq title="What is the difference between SaaS and Self-Hosted?">
      <p>
        If you choose <strong>Gitpod SaaS</strong>, we will manage and host
        Gitpod in the cloud for you. This means minimal setup efforts for you
        and secure data storage in the cloud. Gitpod SaaS is be the best
        solution for teams who want to get started immediately and don’t want to
        spend time on setup and operations.
      </p>
      <p>
        If you choose <strong>Gitpod Self-Hosted</strong>, you will manage and
        host Gitpod on your own instances. This means all data remains your
        infrastructure, as Gitpod can run behind corporate firewalls and on
        air-gapped networks. <strong>Gitpod Self-Hosted</strong> is the best solution
        for teams who want to keep full data control or use Gitpod in private networks.
      </p>
    </Faq>
    <Faq title="How can I install Self-Hosted?">
      <p>
        You can either install <strong>Gitpod Self-Hosted</strong> on
        <a href="/docs/self-hosted/latest/installation/on-gke">Google GKE</a>,
        <a href="/docs/self-hosted/latest/installation/on-amazon-eks"
          >Amazon EKS</a
        >,
        <a href="/docs/self-hosted/latest/installation/on-microsoft-aks"
          >Azure AKS</a
        >
        or
        <a href="/docs/self-hosted/latest/installation/on-kubernetes">K3s</a>.
        See
        <a href="/docs/self-hosted/latest">Self-Hosted Docs</a> for more information.
      </p>
    </Faq>
    <Faq title="How can I pay?">
      <p>
        Currently, <strong>Gitpod Self-Hosted</strong> can only be purchased on
        request. Please <a href="/enterprise-license">request a license key</a>
        and we'll contact you. If you have any questions, please
        <a href="/contact/sales">Get in touch</a>. All our plans can be paid via
        invoice.
      </p>
    </Faq>
    <Faq title="Do you offer discounts for educational institutions?">
      <p>
        Yes, qualified educational institutions may receive a special discount.
        Please <a href="/contact/sales">Contact sales</a>.
      </p>
    </Faq>
    <Faq title="Still have more questions?">
      <p>
        We are happy to answer them, please <a href="/contact/support"
          >Get in Touch</a
        >.
      </p>
    </Faq>
  </Faqs>
</Section>
