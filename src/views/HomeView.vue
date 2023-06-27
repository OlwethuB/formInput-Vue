<template>
<h1>Welcome {{ textarea }}</h1>

  <h2>Text Input</h2>
  <input v-model="text" /> {{ text }}
  <h2>Checkbox</h2>
  <input type="checkbox" id="checkbox" v-model="checked" />
  <label for="checkbox"> Checked: {{ checked }}</label>

  <!-- Multi checkbox -->
  <h2> Multiple checkbox</h2>
  <input v-model="textarea" /> 
  
  <h2>Checkbox</h2>
  <input type="checkbox" id="Frog" v-model="checkedNames" value="Frog" />
  <label for="Frog"> Frog </label>

  <input type="checkbox" id="Deer" v-model="checkedNames" value="Deer"/>
  <label for="Deer"> Deer </label>

  <input type="checkbox" id="Lion" v-model="checkedNames" value="Lion"/>
  <label for="Lion"> Lion </label>

  <p> Checked: 
      <pre> {{ checkedNames }}</pre>
  </p>

  <!-- Making a radio button -->
  <h2>Radio</h2>
  <input type="radio" id="one" value="one" v-model="picked">
  <label for="one">One</label>
  <br>
  <input type="radio" id="two" value="two" v-model="picked">
  <label for="two">Two</label>
  <br>
  <Span> Picked: {{ picked }}</Span>

<!-- multiple selection -->
  <h2> Multiple </h2>
  <select v-model="multiSelected" multiple style="width:100px">
    <option>First</option>
    <option>Second</option>
    <option>Third</option>
    <option>Fourth</option>
    <option>Fifth</option>
    <option>Sixth</option>
    <option>Seventh</option>
    <option>Eighth</option>
    <option>Ninth</option>
    <option>Tenth</option>
  </select>
  <Span> Selected: {{ multiSelected }}</Span>


</template>

<script>
export default {
  data() {
    return {
      text: "",
      // when clicked the boolean will change to true
      checked: true,
      // Shows the inputed arrays
      checkedNames: ['Frog'],
      // the defaulted picked one
      picked: 'one',
      // 
      multiSelected: ['A'],
    };
  },
};
</script>
