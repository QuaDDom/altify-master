<template>
  <div class="container mx-auto">
    <div class="flex justify-between items-center">
      <h1 class="page-title">
        Tickets
      </h1>
    </div>
    <div class="tickets-wrapper">
      <div v-for="[key, ticket] in Object.entries(tickets)" :key="'ticket-' + key" class="ticket">
        <div class="flex justify-center items-center">
          <font-awesome-icon :icon="'fa-brands fa-' + ticket.icon" class="mr-5 text-3xl text-gray-400" />
          <div>
            <h1 class="ticket-title">
              {{ ticket.title }}
            </h1>
            <span class="ticket-timestamp">Last response from {{ ticket.timestamp }}</span>
          </div>
        </div>
        <div v-if="ticket.status === 'unpaid'">
          <span class="tag tag-blue">WAITING FOR PAYMENT</span>
        </div>
        <div v-else-if="ticket.status === 'paid'">
          <span class="tag tag-green">PROCESSING</span>
        </div>
        <div v-if="ticket.status === 'stalled'">
          <span class="tag tag-orange">STALLED</span>
        </div>
        <div v-if="ticket.status === 'closed'">
          <span class="tag tag-dark">CLOSED</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'dashboard',
  data () {
    return {
      tickets: [
        {
          title: 'My PC isn\'t working!',
          timestamp: 'cheaterSK • 28 Feb 2023 14:00',
          status: 'unpaid',
          icon: 'discord'
        },
        {
          title: 'I didn\'t get my account credentials!',
          timestamp: 'cheaterSK • 28 Feb 2023 14:00',
          status: 'paid',
          icon: 'youtube'
        },
        {
          title: 'The website is down!',
          timestamp: 'cheaterSK • 28 Feb 2023 14:00',
          status: 'stalled',
          icon: 'steam'
        },
        {
          title: 'The website is down!',
          timestamp: 'cheaterSK • 28 Feb 2023 14:00',
          status: 'closed',
          icon: 'spotify'
        }
      ]
    }
  }
}
</script>
