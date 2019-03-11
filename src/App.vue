<template>
  <div id="app">

    <nav
      class="navbar is-success is-fixed-top"
      role="navigation"
      aria-label="main navigation"
    >
      <h1>Float Out</h1>
      <span> Current Profit: ${{finalResult}}</span>
    </nav>

    <div class="container content">
      <div class="columns">
        <div class="column is-6 is-offset-3">
          <div class="field">
            <label class="label">5¢</label>
            <div class="control">
              <input
                v-model="fiveCents"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of five cents</p>
          </div>

          <div class="field">
            <label class="label">10¢</label>
            <div class="control">
              <input
                v-model="tenCents"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of ten cents</p>
          </div>

          <div class="field">
            <label class="label">20¢</label>
            <div class="control">
              <input
                v-model="twentyCents"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of twenty cents</p>
          </div>

          <div class="field">
            <label class="label">50¢</label>
            <div class="control">
              <input
                v-model="fiftyCents"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of fifty cents</p>
          </div>

          <div class="field">
            <label class="label">$1</label>
            <div class="control">
              <input
                v-model="oneDollar"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of one dollar</p>
          </div>

          <div class="field">
            <label class="label">$2</label>
            <div class="control">
              <input
                v-model="twoDollar"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of two dollar</p>
          </div>

          <div class="field">
            <label class="label">$5</label>
            <div class="control">
              <input
                v-model="fiveDollar"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of five dollar</p>
          </div>

          <div class="field">
            <label class="label">$10</label>
            <div class="control">
              <input
                v-model="tenDollar"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of ten dollar</p>
          </div>

          <div class="field">
            <label class="label">$20</label>
            <div class="control">
              <input
                v-model="twentyDollar"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of twenty dollar</p>
          </div>

          <div class="field">
            <label class="label">$50</label>
            <div class="control">
              <input
                v-model="fiftyDollar"
                class="input"
                type="number"
                placeholder="total ammount"
              >
            </div>
            <p class="help is-info">Please enter the total number of fifty dollar</p>
          </div>

          <div class="field is-grouped">
            <div class="control">
              <button
                v-on:click="clear"
                class="button is-danger"
              >Clear</button>
            </div>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      fiveCents: "",
      tenCents: "",
      twentyCents: "",
      fiftyCents: "",
      oneDollar: "",
      twoDollar: "",
      fiveDollar: "",
      tenDollar: "",
      twentyDollar: "",
      fiftyDollar: ""
    };
  },

  methods: {
    clear() {
      (this.tenCents = ""),
        (this.fiveCents = ""),
        (this.twentyCents = ""),
        (this.fiftyCents = ""),
        (this.oneDollar = ""),
        (this.twoDollar = ""),
        (this.fiveDollar = ""),
        (this.tenDollar = ""),
        (this.twentyDollar = ""),
        (this.fiftyDollar = "");
    }
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
      return this.fiftyCents * 0.5;
    },

    oneDollarResult: function() {
      return this.oneDollar * 1;
    },

    twoDollarResult: function() {
      return this.twoDollar * 2;
    },
    fiveDollarResult: function() {
      return this.fiveDollar * 5;
    },

    tenDollarResult: function() {
      return this.tenDollar * 10;
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
        this.twoDollarResult +
        this.fiveDollarResult +
        this.tenDollarResult +
        this.twentyDollarResult +
        this.fiftyDollarResult -
        250
      );
    }
  }
};
</script>
<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  padding: 100px 0 0 0;
}
nav {
  display: flex;
  justify-content: space-between;
  padding: 0 1em;
  h1 {
    align-self: center;
    margin: 0;
    font-weight: 600;
  }
  span {
    align-self: center;
    font-weight: 600;
  }
}

.content {
  padding: 0 20px;
}

.button {
  margin: 1em 0 0 0;
}
</style>
