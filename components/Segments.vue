<template>
  <div id="proposito">
    <h2>Nosso Segmentos</h2>
    <div class="p-wrapper">
      <div v-for="card in list" :key="card.title" class="p-card">
        <h4 class="text-primary mb-2">{{ card.title }}</h4>
        <span>
          {{ card.description }}
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          title: "Criação de Sites Profissionais",
          description:
            "Transforme sua ideia em um site incrível! Desenvolvemos sites personalizados que destacam sua marca online.",
        },
        {
          title: "Criação de Blogs Cativantes",
          description:
            "Conteúdo de qualidade é o segredo para o sucesso online. Deixe-nos criar um blog que envolva e informe seu público.",
        },
        {
          title: "Landing Pages de Alta Conversão",
          description:
            "Capture leads e converta visitantes em clientes com nossas landing pages de alta conversão. Resultados garantidos!",
        },
        {
          title: "Consultoria Especializada",
          description:
            "Alcance seus objetivos online com nossa consultoria especializada. Vamos criar uma estratégia personalizada para o seu negócio.",
        },
        {
          title: "SEO Estratégico",
          description:
            "Suba nos rankings de busca e alcance mais clientes. Nosso SEO estratégico coloca você no topo do jogo.",
        },
        {
          title: "Criação de sistemas pernonalizados",
          description:
            "Potencialize seu negócio com sistemas personalizados que se encaixam perfeitamente às suas necessidades. Transforme sua visão em realidade agora",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
#proposito {
  width: 80%;
  margin: auto;

  h2 {
    margin: 32px 0;
  }
  .p-wrapper {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
    @media (max-width: 999px) {
      grid-template-columns: 1fr;
    }
    .p-card {
      border-radius: 16px;
      padding: 16px;
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: center;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1), 0 8px 16px rgba(0, 0, 0, 0.1);
      border: 1px solid #ddd;
      @media (max-width: 999px) {
        width: auto;
        margin-bottom: 16px;
      }
      h4 {
        text-align: center;
      }
      span {
        text-align: center;
        letter-spacing: 1px;
        line-height: 2;
      }
    }
  }
  @media (max-width: 999px) {
    width: 90%;
  }
}
</style>