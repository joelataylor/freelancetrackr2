<template>
  <div class="h-screen flex-auto max-w-2xl mx-auto px-4">

      <header class="flex items-center justify-between z-0 bg-white py-6 border-b">
        <h1 class="font-light text-3xl">
          Clients
        </h1>
        <button class="appearance-none px-4 py-2 bg-green-dark text-green-lightest hover:bg-green rounded-sm">
          New Client
        </button>
      </header>

      <main class="mt-26 pt-8 font-light text-center">
        <div class="flex justify-around">
          <IncomeStatus type="overdue" />
          <IncomeStatus type="outstanding" />
          <IncomeStatus type="draft" />
        </div>

        <div class="flex flex-col mt-8 text-left">
          <h2 class="font-light text-lg mb-4">Client Roster</h2>

          <div class="client-cards">
            <ClientCard :id="4" />
            <ClientCard :id="5" />
            <ClientCard :id="6" />
            <ClientCard :id="4" />
            <ClientCard :id="5" />
            <ClientCard :id="6" />
            <ClientCard :id="4" />
            <ClientCard :id="4" />
          </div>

          <div class="flex flex-col my-8 text-center">
            <div class="flex-1">
              <nuxt-link to="" class="no-underline border-2 border-grey-light hover:bg-grey-light rounded-lg text-xs py-1 px-2 text-grey-darker">
                View Archived Clients</nuxt-link>
            </div>
          </div>
        </div>
      </main>

  </div>
</template>

<script>
import IncomeStatus from '@/components/IncomeStatus'
import ClientCard from '~/components/ClientCard'

export default {
  data() {
    return {
      clientID: null
    };
  },
  methods: {
    goToClient() {
      this.$router.push("/clients/" + this.clientID);
    }
  },
  components: {
    IncomeStatus,
    ClientCard
  }
};
</script>

<style lang="postcss">
  .client-cards {
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 1.5rem;
  }

  @screen lg {
    .client-cards {
      grid-template-columns: 1fr 1fr 1fr;
    }
  }
</style>
