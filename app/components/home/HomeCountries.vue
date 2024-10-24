<script setup lang="ts">
const events = [
  {
    label: "Chicago Halloween Bar Crawl - 10/26",
    value: 1576,
    color: "red",
  },
  {
    label: "Hoboken Halloween Bar Crawl - 10/26",
    value: 1437,
    color: "orange",
  },
  {
    label: "Philadelphia Halloween Bar Crawl - 10/26",
    value: 1368,
    color: "yellow",
  },
  {
    label: "Charlotte Halloween Bar Crawl - 10/26",
    value: 1231,
    color: "green",
  },
  {
    label: "Boston Halloween Bar Crawl - 10/26",
    value: 1145,
    color: "teal",
  },
  {
    label: "Philadelphia Halloween Bar Crawl - 10/25",
    value: 984,
    color: "blue",
  },
  {
    label: "Chicago Halloween Bar Crawl - 10/25",
    value: 871,
    color: "indigo",
  },
  {
    label: "Hoboken Halloween Bar Crawl - 10/25",
    value: 794,
    color: "pink",
  },
];
</script>

<template>
  <UDashboardCard
    title="Top Events"
    description="Top Ticket Sales Across your events."
    icon="i-heroicons-ticket-20-solid"
  >
    <div class="space-y-2">
      <UMeter
        v-for="(event, index) in events"
        :key="index"
        :value="event.value"
        :min="0"
        :max="2000"
        :label="event.label"
        :color="event.color"
        size="lg"
        class="flex-row-reverse items-center"
        :ui="{
          label: { base: 'flex-shrink-0 w-24' },
          indicator: { container: '!w-auto' },
          meter: { base: 'flex-1' },
        }"
        indicator
      />
    </div>
  </UDashboardCard>
</template>
