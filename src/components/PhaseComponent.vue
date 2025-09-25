<template>
  <div class="phase-container" :style="phaseStyle">
    <div class="phase-header">
      <h3 class="phase-title">{{ phaseTitle }}</h3>
    </div>
    <ul class="action-list">
      <li v-for="action in actions" :key="action">{{ action }}</li>
    </ul>
    <p class="phase-text">{{ phaseText }}</p>
  </div>
</template>

<script>
export default {
  props: {
    phaseTitle: String,
    actions: Array,
    phaseText: String,
    phaseColor: String, // e.g., 'blue', 'purple', etc. for background
    // If you were to implement quotes:
    // quote: String,
    // quotePosition: String // 'top', 'bottom', 'left', 'right'
  },
  computed: {
    phaseStyle() {
      return {
        backgroundColor: this.phaseColor,
        // You could also apply gradients here if `phaseColor` was an array or object
      };
    },
    computed: {
      phaseStyle() {
        return {
          backgroundColor: this.phaseColor,
        };
      },
      // Use HTML entity codes for maximum compatibility
    },
    // If implementing quote bubbles:
    // quoteBubbleStyle() {
    //   // Logic to position the quote bubble based on `quotePosition`
    //   return {};
    // }
  },
};
</script>

<style scoped>
.phase-container {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  border-radius: 8px; /* Slightly rounded corners like in the image */
  padding: 20px;
  margin: 10px; /* Space between duplicated components */
  color: white; /* Text color for readability on colored backgrounds */
  flex: 1; /* Allows components to share space if displayed in a flexbox container */
  display: flex;
  flex-direction: column;
  justify-content: space-between; /* Distribute content vertically */
  flex: 1; /* Allows the component to grow and shrink */
  min-width: 150px; /* Sets a minimum width for the component */
  max-width: 300px; /* Optional: sets a maximum width */
}

.phase-header {
  margin-bottom: 15px;
}

.phase-title {
  font-size: 1.5em;
  font-weight: bold;
}

.action-list {
  list-style-type: "→ "; /* Remove default bullet points */
  padding: 0;
  margin: 0 0 20px 5px; /* Space below actions, no left padding */
}

.action-list li {
  margin-bottom: 5px;
}

.phase-text {
  font-size: 0.9em;
  line-height: 1.4;
  /* Adjust padding-top to create space from the action list, as requested */
  padding-top: 15px;
}
.phase-emoticon {
  font-size: 2em; /* Adjust size as needed */
  margin-left: 10px; /* Space between title and emoticon */
  line-height: 1; /* Ensures it sits nicely on the line */
}

.phase-header {
  display: flex; /* Use flexbox to align title and emoticon */
  align-items: center; /* Vertically center them */
  margin-bottom: 15px;
}
/* For the rainbow effect across multiple components, you'd define specific colors */
/* Example for main app or parent component usage */
/*
.parent-container {
  display: flex;
  flex-wrap: wrap;
}
*/
</style>
