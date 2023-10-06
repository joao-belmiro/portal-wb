<template>
  <div class="p-container">
    <h2>Propósito</h2>
    <div class="p-list">
      <div class="column">
        <div class="item-list">Alcance global</div>
        <div class="item-list">Marketing eficiente</div>
        <div class="item-list">Construção de marca</div>
        <div class="item-list">Atender necessidades únicas</div>
      </div>

      <div class="column">
        <div class="item-list">Compartilhar conhecimento</div>
        <div class="item-list">Engajar audiência</div>
        <div class="item-list">Monetização potencial</div>
        <div class="item-list">Automatizar processos</div>
      </div>
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
    justify-content: center;
    align-items: center;
    margin-left: 24px;
    margin-top: 32px;
    gap: 5%;
    width: 95%;
    @media (max-width: 700px) {
      gap: 0;
      width: 100%;
      flex-direction: column;
      align-items: flex-start;
    }
    .column {
      width: 95%;
      .item-list {
        box-shadow: 0.25rem 0.25rem 0.6rem rgba(0, 0, 0, 0.05),
          0 0.5rem 1.125rem rgba(75, 0, 0, 0.05);
        position: relative;
        text-align: start;
        font-size: 18px;
        margin-bottom: 24px;
        padding: 12px 32px;
        border-radius: 16px;
        border: 1px solid #ddd;
        @media (max-width: 700px) {
          font-size: 14px;
        }
        &::before {
          padding: 4px 8px;
          background: #add8e6;
          border-radius: 1rem 1rem 0 1rem;
          position: absolute;
          left: -24px;
          top: -20px;
          content: url("@/assets/images/check-circle.svg");
        }
      }
    }
  }
  @media (max-width: 999px) {
    width: 90%;
  }
}
</style>