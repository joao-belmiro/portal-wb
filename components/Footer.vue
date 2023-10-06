<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="column">
        <p>CNPJ: 47.398.732/0001-45</p>
        <p>Email: joao_belmiro@hotmail.com</p>
        <p>Telefone: (91) 98352-9700</p>
      </div>
      <div class="column">
        <p>Belém</p>
        <p>Pará</p>
        <p>Passagem D'hotel, 350</p>
        <p>CEP: 66080-210</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped lang="scss">
.footer {
  background-color: $primary;
  color: $background;
  padding: 30px 0;
  text-align: left;
  width: 100%;
}

.footer-content {
  max-width: 80%;
  margin: 0 auto;
  display: flex;

  align-items: flex-start;
}

.column {
  flex: 1;
  text-align: left;
  margin: 10px 0; 
}

.column p {
  margin: 0;
  font-size: 16px;
}

@media (max-width: 768px) {
  .footer-content {
    flex-direction: column; 
  }
  .column {
    flex: none;
  }
}
</style>
