<template>
  <div class="card-container d-flex justify-content-center">
    <div v-for="(sport, index) in sports" :key="index" class="card-item">
      <div class="card">
        <img
          :src="sport.img"
          alt=""
          style="width: 200px; height: 200px; object-fit: cover"
        />
        <div class="card-body">
          <h5 class="card-title">{{ sport.name }} - {{ sport.price}}$</h5>
          <p class="card-text">{{ sport.description }}</p>
          <div @click="totalprice" class="btn btn-primary">Add More</div>
          <h5>Total: {{ total }}</h5>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sports: [
        {
          name: "Real Madrid",
          price: 17,
          description: "Real Madrid adidas Home Shirt 2023-24",
          img: require("./img/real.jpg"),
        },
        {
          name: "Barcelona",
          price: 18,
          description: "Barcelona adidas Home Shirt 2023-24",
          img: require("./img/fcb.jpg"),
        },
        {
          name: "Arsenal",
          price: 15,
          description: "Arsenal adidas Home Shirt 2023-24",
          img: require("./img/arsernal.jpg"),
        },
        {
          name: "Man City",
          price: 14,
          description: "Man City adidas Home Shirt 2023-24",
          img: require("./img/man city.jpg"),
        },
      ],
      total: "",
    };
  },
  methods: {
    totalprice() {
      this.total = 'Hi';
    },
  },
};
</script>

<style>

</style>