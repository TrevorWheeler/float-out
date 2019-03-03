<template>
  <div>
    <form>
      <p>5 cents</p>
      <input
        style="border:2px solid grey;"
        type="number"
        v-model="fiveCents"
        placeholder="5 cents"
      />

      <p>10 cents</p>

      <input
        style="border:2px solid grey;"
        type="number"
        v-model="tenCents"
        placeholder="10 cents"
      />
      <p>20 cents</p>

      <input
        style="border:2px solid grey;"
        type="number"
        v-model="twentyCents"
        placeholder="20 cents"
      />

      <p>50 cents</p>

      <input
        style="border:2px solid grey;"
        type="number"
        v-model="fiftyCents"
        placeholder="50 cents"
      />

      <p>1 Dollar</p>

      <input
        style="border:2px solid grey;"
        type="number"
        v-model="oneDollar"
        placeholder="one dollar"
      />

      <p>5 Dollar</p>

      <input
        style="border:2px solid grey;"
        type="number"
        v-model="fiveDollar"
        placeholder="5 dollars"
      />

      <p>20 Dollar</p>

      <input
        style="border:2px solid grey;"
        type="number"
        v-model="twentyDollar"
        placeholder="20 dollars"
      />
      <p>50 Dollar</p>

      <input
        style="border:2px solid grey;"
        type="number"
        v-model="fiftyDollar"
        placeholder="50 dollars"
      />
    </form>
    <hr>
    <h1>${{finalResult}}</h1>

  </div>
</template>

<script>
export default {
  name: "home",
  data() {
    return {
      fiveCents: "",
      tenCents: "",
      twentyCents: "",
      fiftyCents: "",
      oneDollar: "",
      fiveDollar: "",
      twentyDollar: "",
      fiftyDollar: ""
      // result: ""
    };
  },

  computed: {
    fiveCentsResult: function() {
      return this.fiveCents * 0.05;
    },
    tenCentsResult: function() {
      return this.tenCents * 0.1;
    },
    twentyCentsResult: function() {
      return this.twentyCents * 0.2;
    },

    fiftyCentsResult: function() {
      return this.fiftyCents / 0.5;
    },

    oneDollarResult: function() {
      return this.oneDollar * 1;
    },
    fiveDollarResult: function() {
      return this.fiveDollar * 5;
    },

    twentyDollarResult: function() {
      return this.twentyDollar * 20;
    },

    fiftyDollarResult: function() {
      return this.fiftyDollar * 50;
    },

    finalResult: function() {
      return (
        this.tenCentsResult +
        this.fiveCentsResult +
        this.twentyCentsResult +
        this.fiftyCentsResult +
        this.oneDollarResult +
        this.fiveDollarResult +
        this.twentyDollarResult +
        this.fiftyDollarResult -
        250
      );
    }
  }
};
</script>

<style>
input {
  border: 2px solid grey;
}
</style>

