<template>
  <div class="contact-form">
    <h2 class="text-primary">Envie sua mensagem</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="nome">Nome</label>
        <input
          type="text"
          id="nome"
          v-model="formData.nome"
          @focus="inputFocus"
          @blur="inputBlur"
          required
        />
      </div>
      <div class="form-group">
        <label for="email">Seu melhor e-mail</label>
        <input
          type="email"
          id="email"
          v-model="formData.email"
          @focus="inputFocus"
          @blur="inputBlur"
          required
        />
      </div>
      <div class="form-group">
        <label for="telefone">Whatsapp</label>
        <input
          type="tel"
          id="telefone"
          v-model="formData.telefone"
          @focus="inputFocus"
          @blur="inputBlur"
          required
        />
      </div>
      <div class="form-group">
        <label for="descricao">Mensagem</label>
        <textarea
          id="descricao"
          v-model="formData.descricao"
          rows="6"
          
          @focus="inputFocus"
          @blur="inputBlur"
          required
        ></textarea>
        <p class="count">
        <span id="charCount">{{ formData.descricao.length }}</span>
        </p>
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
      console.table(this.formData);
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
  max-width: 60%;
  margin: 20px auto;
  padding: 20px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  @media (max-width: 999px) {
    max-width: 90%;
  }
  h2 {
    font-size: 1.5rem;
    text-align: center;
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
      border: none;
      flex: 1;
      border-bottom: 3px solid $secondary;
      border-radius: 8px 8px 0 0;

      &:focus-within {
        outline: none;
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
    background-color: $primary;
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    align-self: flex-start;
    &:hover {
      opacity: 0.7;
    }
  }
  .count {
    text-align: right;
    font-size: 12px;
    color: $grey-1 !important;
  }
}
</style>