<template>
  <div id="sobre" class="sobre">
    <span>
      fabrica de sites é uma agência de desenvolvimento web localizada em
      Abaetetuba, PA. Nossa equipe altamente qualificada oferece soluções
      personalizadas para atender às necessidades únicas do seu negócio. Do
      design ao desenvolvimento, estamos comprometidos em criar sites
      profissionais e funcionais que impulsionem o crescimento da sua empresa.
      Trabalhamos de perto com você para entender sua visão e transformá-la em
      realidade, garantindo uma presença online impactante e eficaz. Confie na
      fabrica de sites para construir uma presença digital de sucesso para o seu
      negócio.
    </span>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.sobre {
  letter-spacing: 1px;
  line-height: 2;
  font-size: 20px;
  margin: 20px auto ;
  text-align: center;
  width: 80%;
  color: $dark;
  @media (max-width: 999px) {
    padding-top: 14px;
    font-size: 14px;
    width: 90%;
  }
  span {
    width: 80%;
  }
}
</style>