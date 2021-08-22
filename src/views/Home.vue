<template>
  <h1>Events For Good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
  
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard,
  },
  data() {
    return {
      events: [
        {
          id: 123456,
          category: 'animal welfare',
          title: 'Dog Adoption Day',
          description: 'Find your new k9 friend at this event.',
          location: 'Wof! Town',
          date: 'January 01, 2022',
          time: '12:00',
          petsAllowed: true,
          organizer: 'John Wick'
        },
        {
          id: 9876543,
          category: 'animal cruelty',
          title: 'Dog Kidnapping Day',
          description: 'Let us steal your k9 friend at this event.',
          location: 'Wof! Town',
          date: 'January 01, 2022',
          time: '12:00',
          petsAllowed: true,
          organizer: 'Cruella De Vil'
        },
        {
          id: 3214567,
          category: 'animal loving',
          title: 'Dog Loving Day',
          description: 'Let us give your k9 a hug at this event.',
          location: 'Wof! Town',
          date: 'January 01, 2022',
          time: '12:00',
          petsAllowed: true,
          organizer: 'Adorable Kids'
        }
      ]
    }
  }
};
</script>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>