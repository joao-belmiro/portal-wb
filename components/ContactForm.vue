<template>
  <div class="contact-form">
    <h2 class="text-primary">
      Entre em Contato conosco</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="nome">Nome:</label>
        <input
          type="text"
          id="nome"
          v-model="formData.nome"
          @focus="inputFocus"
          @blur="inputBlur"
        />
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input
          type="email"
          id="email"
          v-model="formData.email"
          @focus="inputFocus"
          @blur="inputBlur"
        />
      </div>
      <div class="form-group">
        <label for="telefone">Telefone:</label>
        <input
          type="tel"
          id="telefone"
          v-model="formData.telefone"
          @focus="inputFocus"
          @blur="inputBlur"
        />
      </div>
      <div class="form-group">
        <label for="descricao">Descrição:</label>
        <textarea
          id="descricao"
          v-model="formData.descricao"
          rows="6"
          @focus="inputFocus"
          @blur="inputBlur"
        ></textarea>
        <p style="text-align:right;">0/ <span id="charCount">{{formData.descricao.length}}</span></p>
      </div>
      <button type="submit">Enviar</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        nome: "",
        email: "",
        telefone: "",
        descricao: "",
      },
      inputFocused: false,
    };
  },
  methods: {
    submitForm() {
      // Lógica para enviar o formulário
      console.log("Dados do formulário:", this.formData);
      // Aqui você pode enviar os dados do formulário para o servidor ou executar qualquer outra ação necessária
    },
    inputFocus() {
      this.inputFocused = true;
    },
    inputBlur() {
      this.inputFocused = false;
    },
  },
};
</script>

<style scoped lang="scss">
.contact-form {
  max-width: 70%;
  margin: 20px auto;
  padding: 20px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;

  h2 {
    font-size: 1.5rem;
    margin-bottom: 20px;
  }

  .form-group {
    margin-bottom: 20px;
    display: flex;
    flex-direction: column;

    label {
      color: $dark;
      font-weight: bold;
      margin-bottom: 5px;
    }
    input,
    textarea {
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 8px;
      flex: 1;

      &:focus-within {
        outline: none;
        border: 1px solid $secondary; /* Substitua $primary pela sua variável de cor */
      }
    }

    textarea {
      resize: vertical;
    }
  }

  .input-row {
    display: flex;

    .form-group {
      flex: 1;
      margin-right: 10px;
    }
  }

  button {
    background-color: $primary; /* Substitua $primary pela sua variável de cor */
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    align-self: flex-start;
  }
}
</style>