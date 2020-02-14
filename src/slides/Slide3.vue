<template>
  <section class="slide3">
    <Page>
      <Title>CSS анимации</Title>
      <SubTitle>Особенности</SubTitle>
      <Layout>
        <Rows class="slide3-rows">
          <List :items="animationsList" class="slide3-list"/>
          <section class="slide3-examples">
            <div class="slide3-example example">
              <div class="example-label">отступ</div>
              <div class="example-box example-box--1"></div>
            </div>
            <div class="slide3-example example">
              <div class="example-label">цвет и ширина</div>
              <div class="example-box example-box--2"></div>
            </div>
            <div class="slide3-example example">
              <div class="example-label">прозрачность</div>
              <div class="example-box example-box--3"></div>
            </div>
            <div class="slide3-example example">
              <div class="example-label">поворот и скругление углов</div>
              <div class="example-box example-box--4"></div>
            </div>
            <div class="slide3-example example">
              <div class="example-label">3d перспектива</div>
              <div class="example-box example-box--5"></div>
            </div>
          </section>
        </Rows>
      </Layout>
    </Page>
  </section>
</template>

<script>
import Layout from '@/components/Layout.vue';
import List from '@/components/List.vue';
import Page from '@/components/Page.vue';
import Rows from '@/components/Rows.vue';
import SubTitle from '@/components/SubTitle.vue';
import Title from '@/components/Title.vue';

export default {
  name: 'Slide3',
  components: {
    Layout,
    List,
    Page,
    Rows,
    SubTitle,
    Title,
  },
  data() {
    return {
      animationsList: [
        { main: 'Позволяют анимировать одно или несколько свойств элемента' },
        { main: 'Можно анимировать все свойства, которые имеют численное значение' },
        { main: 'Позволяют анимировать большинство интерфейсных элементов' },
        { main: 'Поддерживаются нативно (не требуют писать дополнительного кода для реализации)' },
        { main: 'Функция движения описывается кривой безье, или по шагам' },
      ],
    };
  },
};
</script>

<style lang="postcss" scoped>
.slide3 {

  &-rows {
    justify-self: center;
    max-width: 960px;
  }

  &-list {
    font-size: 2vw;

    @media (max-width: 1024px) {
      font-size: 5vw;
    }
  }
}

.example {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  margin-left: 60px;

  @media (max-width: 1024px) {
    flex-direction: column;
    margin-left: 1em;
    align-items: flex-start;
  }

  &-label {
    font-weight: 600;
  }

  &-box {
    margin: 1em;
    width: 60px;
    height: 60px;
    position: relative;
    background-color: #c81212;

    &--1 {
      animation-name: animation1;
      animation-duration: 2s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      animation-timing-function: ease-in;
    }

    @keyframes animation1 {
      to {
        margin-left: 12em;
      }
    }

    &--2 {
      animation-name: animation2;
      animation-duration: 4s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
    }

    @keyframes animation2 {
      to {
        width: 60%;
        background-color: #2c3e50;
      }
    }

    &--3 {
      animation-name: animation3;
      animation-duration: 3s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
    }

    @keyframes animation3 {
      to {
        opacity: 0;
      }
    }

    &--4 {
      animation-name: animation4;
      animation-duration: 1s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      animation-timing-function: cubic-bezier(.58,-0.79,0,.91);
    }

    @keyframes animation4 {
      from {
        border-radius: 0px;
      }

      to {
        transform: rotate(45deg);
        border-radius: 30px;
      }
    }

    &--5 {
      animation-name: animation5;
      animation-duration: 3s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
    }

    @keyframes animation5 {
      to {
        transform: perspective(60px) rotateX(180deg);
      }
    }
  }
}
</style>
