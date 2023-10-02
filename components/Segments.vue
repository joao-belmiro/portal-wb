<template>
  <div id="proposito">
    <h2>Nosso propósito</h2>
    <div class="p-wrapper">
      <div class="p-card">
        <img src="@/assets/images/notebook.svg" alt="" />
        <span>
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500s, when an unknown printer took a galley of type and
          scrambled it to make a type specimen book.
        </span>
      </div>
      <div class="p-card">
        <img src="@/assets/images/growth.svg" alt="" />
        <span>
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500s, when an unknown printer took a galley of type and
          scrambled it to make a type specimen book.
        </span>
      </div>
      <div class="p-card">
        <img src="@/assets/images/growth.svg" alt="" />
        <span>
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500s, when an unknown printer took a galley of type and
          scrambled it to make a type specimen book.
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
#proposito {
  width: 80%;
  margin: auto;

  h2 {
    margin: 32px 0;
  }
  .p-wrapper {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: flex-start;
    flex-wrap: nowrap;
    gap: 2%;
    .p-card {
      width: 30%;
      border-radius: 16px;
      padding: 16px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1), 0 8px 16px rgba(0, 0, 0, 0.1);
      img {
        width: 150px;
        height: 150px;
      }
    }
  }
}
</style>