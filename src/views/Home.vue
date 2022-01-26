<template>
  <div class="home">
    <section class="hero">
      <div class="hero-text container">
        <h4>Vue Responsive Nav Menu</h4>
        <hr />
        <h2>
          With Vue <br />
          Animations
        </h2>
        <hr />
      </div>
    </section>
    <section>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iste porro eos blanditiis labore corporis officia sapiente adipisci delectus earum autem ut reprehenderit eveniet animi fugiat in inventore,
        pariatur dolor ullam quo neque tempore esse cupiditate! Optio expedita possimus vitae cum quo nam incidunt perspiciatis at excepturi vel ullam, provident, id velit ratione eveniet assumenda voluptatem explicabo quisquam.
        Id temporibus rem fugiat! Nihil hic ut voluptas a suscipit harum exercitationem alias qui possimus nemo molestias tempore provident ipsa odit,
        dolore laudantium ratione eum. Necessitatibus, fuga. Architecto esse, voluptate cupiditate a iure maiores aut delectus deleniti, itaque debitis quo aspernatur.
        Quis enim architecto voluptas atque totam debitis ipsam, dignissimos officia nemo. Cumque sequi alias eaque amet qui dicta magnam numquam deserunt.
        Provident iste id officia asperiores facilis error cumque, odio rem est architecto sit vitae voluptatum facere blanditiis, eaque fugiat obcaecati!
        Nobis ipsum asperiores voluptatibus quae eligendi quam qui. Possimus quas vel explicabo cum enim dolores sint illo fuga assumenda adipisci, 
        recusandae laboriosam quasi deserunt neque accusantium repellat? Corporis quae sapiente autem dolores omnis consequatur earum.
        Delectus consequuntur hic eum, ipsa laudantium, dolor, officia architecto ab illum blanditiis vero beatae sapiente accusantium ut autem voluptas asperiores? 
        Laborum sit perferendis animi soluta dolore!
      </p>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  components: {
   
  }
}
</script>

<style lang="scss" scoped>
.hero {
  background-image: url("../assets/hero-bg.png");
  background-attachment: fixed;
  position: relative;
  height: 100vh;

  img {
    object-fit: cover;
    height: 100%;
    width: 100%;
  }

  .hero-text {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: #fff;

    h4 {
      text-transform: uppercase;
      font-size: 22px;
      padding-bottom: 4px;
    }

    h2 {
      font-size: 50px;
      @media (min-width: 550px) {
        font-size: 80px;
      }
    }

    hr:nth-child(2) {
      max-width: 365px;
      margin-bottom: 16px;
    }
    hr:nth-child(4) {
      height: 6px;
      background-color: #fff;
      border: none;
      max-width: 85px;
      margin-top: 16px;
    }
  }
}
</style>

