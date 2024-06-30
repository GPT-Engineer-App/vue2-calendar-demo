<template>
  <div id="app">
    <FullCalendar :options="calendarOptions" />
  </div>
</template>

<script>
import FullCalendar from '@fullcalendar/vue';
import dayGridPlugin from '@fullcalendar/daygrid';

export default {
  name: 'App',
  components: {
    FullCalendar,
  },
  data() {
    return {
      calendarOptions: {
        plugins: [dayGridPlugin],
        initialView: 'dayGridMonth',
        events: [
          { title: 'event 1', date: '2023-10-01' },
          { title: 'event 2', date: '2023-10-02' },
        ],
      },
    };
  },
};
</script>

<style>
@import '@fullcalendar/common/main.css';
@import '@fullcalendar/daygrid/main.css';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>