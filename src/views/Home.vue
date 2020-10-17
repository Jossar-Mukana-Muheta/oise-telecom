<template>
    <article class="home">
        <header>
          <div class="texte_presentaion">
            <h1>Réparation || Vente  Télephone Portable</h1>
            <p>Retrouver nos 2 boutiques de Creil et Clermont, pour la réparation, achat et revente de vos smartphone, pc et tablette </p>
            <div class="button">
              <Button titre="Nos Magasin" lien="/Boutique"/>
            </div>
          </div>
          <div class="image">
            <ImageHeartbeat/>
          </div>
        </header>
    </article>

</template>

<script>
// @ is an alias to /src


import ImageHeartbeat from "@/components/ImageHeartbeat";
import Button from "@/components/Layout/Button";
export default {
  name: 'Home',
  components: {
    Button,
    ImageHeartbeat

  }
}
</script>
<style lang="scss" scoped>


  header{
    margin-top: 50px;
    margin-right: 5%;
    margin-left: 5%;
    display: flex;
    flex-direction: column;
    align-items: center;


    @include desktop{
      margin-top: 100px;
      margin-right: 15%;
      margin-left: 15%;
      flex-direction: row;
      justify-content: space-between;
    }

    .image{
        display: none;
      @include desktop{
        display: block;
      }

    }
  }

  .texte_presentaion{
    display: flex;
    flex-direction: column;
    align-items: start;
    overflow: hidden;
  }

  @keyframes slider {
    from{
      transform: translateX(-500px);
    }
    to{
      transform: translateX(0px);
    }
  }

  h1{
      font-size: 33px;
    @include desktop{
      font-size: 50px;
      margin-bottom: 0.5em;
      font-weight: 700;
      line-height: 1.2;
      animation: slider 4s 2;
      animation-direction: alternate;

    }
  }

  p{
    color: $p-grey;
    font-size: 17px;
    line-height: 1.6;
    font-weight: 400;
    margin-bottom: 60px;
    padding-right: 50px;
    animation: slider 4s 2;
    animation-direction: alternate;
    animation-delay: 2s;
  }

  .button{
    animation: slider 4s 2;
    animation-direction: alternate;
    animation-delay: 3s;
  }

</style>
