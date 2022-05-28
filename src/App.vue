<template>
  <div id="app">
    <main>
      <div class="search-box">
        <input
          type="text"
          class="search-bar"
          name="search-bar"
          placeholder="Search..."
        />
      </div>
      <div class="weather-wrap">
        <div class="location-box">
          <div class="location">Northampton, UK</div>
          <div class="date">Saturday, May 28, 2022</div>
        </div>
        <div class="weather-box">
          <div class="temp">9°C</div>
          <div class="weather">Rain</div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      api_key: "3f8810bffb0936b0e1325f7a81197318",
    };
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: "montserrat", sans-serif;
}
#app {
  background-image: url("./assets/cold-bg.jpg");
  background-size: cover;
  background-position: bottom;
  transition: 0.1s;
}
main {
  min-height: 100vh;
  padding: 25px;
  background-image: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0.25),
    rgba(0, 0, 0, 0.75)
  );
}
.search-box {
  width: 100%;
  margin-bottom: 30px;
  .search-bar {
    display: block;
    width: 100%;
    padding: 15px;
    color: #313131;
    font-size: 20px;
    appearance: none;
    box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.25);
    border: none;
    outline: none;
    background: none;
    background-color: rgba(255, 255, 255, 0.5);
    border-radius: 0px 16px 0px 16px;
    transition: 0.4s;
    &:focus {
      box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.25);
      background-color: rgba(255, 255, 255, 0.75);
      border-radius: 16px 0px 16px 0px;
    }
  }
}
.weather-wrap {
  .location-box {
    .location {
      color: #fff;
      font-size: 32px;
      font-weight: 500;
      text-align: center;
      text-shadow: 1px 3px rgba(0, 0, 0, 0.25);
    }
    .date {
      color: #fff;
      font-size: 20px;
      font-weight: 300;
      text-align: center;
      font-style: italic;
    }
  }
  .weather-box {
    text-align: center;
    .temp {
      display: inline-block;
      padding: 10px 25px;
      color: #fff;
      font-size: 102px;
      font-weight: 900;
      text-shadow: 3px 6px rgba(0, 0, 0, 0.25);
      background-color: rgba(255, 255, 255, 0.25);
      margin: 30px 0px;
      border-radius: 16px;
      box-shadow: 3px 6px rgba(0, 0, 0, 0.25);
    }
    .weather {
      color: #fff;
      font-size: 48px;
      font-weight: 700;
      font-style: italic;
      text-shadow: 3px 6px rgba(0, 0, 0, 0.25);
    }
  }
}
</style>
