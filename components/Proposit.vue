<template>
  <div class="p-container">
    <h2>Propósito</h2>
    <div class="p-list">
      <ul>
        <li>Alcance global</li>
        <li>Marketing eficiente</li>
        <li>Construção de marca</li>
        <li>Atender necessidades únicas</li>
      </ul>

      <ul>
        <li>Compartilhar conhecimento</li>
        <li>Engajar audiência</li>
        <li>Monetização potencial</li>
        <li>Automatizar processos</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.p-container {
  margin: 20px auto;
  width: 80%;
  display: flex;
  flex-direction: row;
  align-items: center;
  flex-wrap: wrap;
  h2 {
    margin: 20px 0;
    width: 100%;
  }
  .p-list {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    width: 100%;
    @media (max-width: 700px) {
      flex-direction: column;
      align-items: flex-start;
    }
    ul {
      list-style: url("@/assets/images/check-circle.svg");
      li {
        text-align: start;
        font-size: 20px;
        margin-bottom: 12px;
        @media (max-width: 700px) {
          margin-left: 30px;
          font-size: 16px;
        }
      }
    }
  }
}
</style>