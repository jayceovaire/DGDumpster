<template>
  <h1 id="dCostLabel" class="dCostLabel">Dumpster Rental Cost Estimator</h1>
  <div id="calculator" class="calculator">
    <label for="calculator-field">Dumpster Size</label>
    <div class="calculator-field">
      <div class="size-buttons">
        <v-btn
            :class="{ 'selected': selectedDumpsterSize === '10' }"
            @click="selectDumpsterSize('10')"
        >
          10 cubic yards
        </v-btn>
        <v-btn
            :class="{ 'selected': selectedDumpsterSize === '15' }"
            @click="selectDumpsterSize('15')"
        >
          15 cubic yards
        </v-btn>
        <v-btn
            :class="{ 'selected': selectedDumpsterSize === '20' }"
            @click="selectDumpsterSize('20')"

        >
          20 cubic yards
        </v-btn>
      </div>

    </div>
    <label for="rental-days">Rental Days</label>
    <div class="sliderField">
        <v-slider
            class="sliderBar"
            v-model="rentalDays"
            min="5"
            max="10"
            step="1"
            show-ticks
            @input="calculateCost"
        ></v-slider>
        <v-text-field
          class="sliderDaysNumber"
          v-model="rentalDays"
          density="compact"
          type="number"
          hide-details
          single-line
      ></v-text-field>
    </div>
    <div  class="result">
      <p><strong>Total Cost:</strong> ${{ totalCost }}</p>
    </div>
    <div class="disclaimer">
      <i>All dumpster rentals are up to 5 days with a 2 ton weight limit. Rentals exceeding 5 days may be charged a daily rate.</i>
    </div>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue';

const selectedDumpsterSize = ref('10'); // Default selected dumpster size
const rentalDays = ref(5); // Default rental days
const totalCost = ref(325); // Variable to hold the calculated total cost
const perDayCost = 20;

function selectDumpsterSize(size) {
  selectedDumpsterSize.value = size;
  calculateCost();
}

function calculateCost() {
  let total = 0;

  const extraDays = rentalDays.value - 5;
  const extraRentalDaysCost = extraDays > 0 ? extraDays * perDayCost : 0;

  if (selectedDumpsterSize.value === '10') {
    total = 325 + extraRentalDaysCost;
  } else if (selectedDumpsterSize.value === '15') {
    total = 375 + extraRentalDaysCost;
  } else if (selectedDumpsterSize.value === '20') {
    total = 425 + extraRentalDaysCost;
  }

  totalCost.value = total.toFixed(2); // Store total cost, rounded to 2 decimal places
}

// Watch rentalDays to recalculate cost whenever it changes
watch(rentalDays, calculateCost);
</script>

<style scoped>
.calculator {
  max-width:50%;
  margin: 0 auto;

  margin-bottom: 2.5%;
  padding: 2%;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: column;
}

.calculator-field {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

h1 {
  text-align: center;
  margin-bottom: 20px;
  color: black;
}

label {
  color: black;
}


button {
  padding: 10px;
  margin: 5px;
  background-color: #e21d45;
  border: 1px solid #e51d45;
  border-radius: 4px;
  cursor: pointer;
}

button.selected {
  background-color: #67bc45;
  color: black;
}

button:hover {
  background-color: #ddd;
}

button.selected:hover {
  background-color: rgba(103, 188, 69, 0.86);
}

.result {
  margin-top: 20px;
  padding: 10px;
  background-color: #b8f3a0;
  border: 1px solid #ccc;
  border-radius: 4px;
  color: black;
}

.size-buttons {
  display: flex;
  flex-direction: row;
  padding: 2%;
  margin-bottom: .5%;
}


.sliderField {
  display: flex;
  flex-direction: row;
  color: black;
  margin-top: 2%;

}


.sliderField .sliderDaysNumber {
  flex: 0 0 15%;
  color: black;
}

.sliderDaysNumber {
  width: 25%;
  color: black;
}




.disclaimer {
  color: black;
}

/* Media Queries */
@media screen and (max-width: 768px) {
  .calculator {
    max-width: 80%;
  }

  .size-buttons {
    flex-wrap: wrap;
  }

  .sliderDaysNumber {
    width: 40%; /* Adjust width for smaller screens */
  }
}

@media screen and (max-width: 480px) {
  .calculator {
    max-width: 90%;
  }

  h1 {
    font-size: 1.5rem; /* Adjust heading size */
  }

  .sliderDaysNumber {
    width: 60%; /* Further adjust width for smaller screens */
  }

  #dCostLabel {
    font-size: xx-large;
  }


}

.dCostLabel {
  color: #eb1c25;
  font-size: xxx-large;
  margin-top: 15%;
}

</style>



