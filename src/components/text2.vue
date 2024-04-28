<template>
  <h1>Гайд по сборке компьютера</h1>
  <p class="pHead">
    Если вы не хотите выполнять сборку у нас, вы можете приобрести комплектующие у нас и самостоятельно выполнить сборку системного блока.
    Для этого мы подготовили для вас пошаговую инструкцию как выполнить сборку. 
  </p>
  <main>
    <section>
        <h2>Подготовка</h2>
        <p>Перед началом сборки убедитесь, что у вас есть все необходимые компоненты: процессор, материнская плата, оперативная память, видеокарта, жесткий диск или SSD, блок питания, корпус, клавиатура, мышь и монитор.</p>
    </section>

    <section>
        <h2>Шаги сборки</h2>
        <ol>
            <li>Установите процессор на материнскую плату, следуя инструкциям производителя.</li>
            <li>Установите оперативную память в слоты на материнской плате.</li>
            <li>Установите видеокарту в соответствующий слот.</li>
            <li>Подключите жесткий диск или SSD к материнской плате и блоку питания.</li>
            <li>Установите блок питания в корпус и подключите его к материнской плате, видеокарте и другим компонентам.</li>
            <li>Установите материнскую плату в корпус, зафиксируйте ее и подключите все необходимые кабели.</li>
            <li>Установите клавиатуру, мышь и другие периферийные устройства.</li>
            <li>Подключите монитор к видеокарте.</li>
        </ol>
    </section>

    <section>
        <h2>Тестирование и настройка</h2>
        <p>После завершения сборки убедитесь, что все компоненты правильно подключены. Затем включите компьютер и выполните первоначальную настройку BIOS. После этого установите операционную систему и драйверы для всех устройств.</p>
    </section>

    <section>
        <h2>Завершение</h2>
        <p>Поздравляем, ваш компьютер собран и готов к использованию! Наслаждайтесь новой системой и не забудьте регулярно обновлять драйверы и проводить техническое обслуживание.</p>
    </section>

    <section>
        <h1 style="padding-left: 0;">Видео-инструкция</h1>
        <YouTube class="youtube"
        src="https://www.youtube.com/watch?v=L9ZwCLNAW4A&t=3s" 
        ref="youtube" />
    </section>

</main>
</template>

<style scoped>

.youtube {
  padding-left: 25%;
  padding-right: 25%;
}

main {
  padding-top: 30px;
  text-align: left;
  padding-left: 7%;
  text-transform: uppercase;
  font-weight: 100;
  line-height: 2;
  color: #2c3e50;
}

h1 {
  padding-top: 30px;
  text-align: center;
  padding-left: 7%;
  text-transform: uppercase;
  font-weight: 100;
  line-height: 2;
  color: #2c3e50;
}

.pHead{
  padding-top: 30px;
  text-align: left;
  padding-left: 7%;
  text-transform: uppercase;
  font-weight: 100;
  line-height: 2;
  color: #2c3e50;
}


</style>

<script>
import { defineComponent } from 'vue'
import YouTube from 'vue3-youtube'

export default defineComponent({
    components: { YouTube },
    methods: {
        onReady() {
            this.$refs.youtube.playVideo()
        },
    },
});
</script>