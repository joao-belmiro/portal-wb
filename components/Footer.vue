<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="column">
        <p>CNPJ: 12.345.678/0001-90</p>
        <p>Email: exemplo@email.com</p>
        <p>Telefone: (123) 456-7890</p>
      </div>
      <div class="column">
        <p>Email: exemplo@email.com</p>
        <p>Cidade: Sua Cidade</p>
        <p>Estado: Seu Estado</p>
        <p>Rua: Nome da Rua, 123</p>
        <p>CEP: 12345-678</p>
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
  background-color: $primary; /* Substitua $background pela sua variável de cor */
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
  margin: 10px 0; /* Espaço entre as colunas */
}

.column p {
  margin: 0;
  font-size: 16px;
}

/* Adicione regras de mídia para tornar o footer responsivo */
@media (max-width: 768px) {
  .footer-content {
    flex-direction: column; /* Empilha as colunas uma acima da outra */
  }
  .column {
    flex: none; /* Remove a flexibilidade para que as colunas não se estendam horizontalmente */
  }
}
</style>
