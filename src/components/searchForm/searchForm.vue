<template>
  <div>
    <form class="mt-8">
      <md-card class="md-layout-item md-size-50 md-small-size-100  ml-auto">
        <md-card-content>
          <div class="md-layout md-gutter">
            <div class="md-layout-item">
              <md-field>
                <label for="caller">Звонящая сторона (Caller)</label>
                <md-select v-model="caller" name="caller" id="caller">
                  <md-option value="kz">Казахстан (kz)</md-option>
                  <md-option value="ru">Россия (ru)</md-option>
                  <md-option value="de">Германия (de)</md-option>
                  <md-option value="us">США (us)</md-option>
                </md-select>
              </md-field>
            </div>
          </div>
          <div class="md-layout md-gutter">
            <div class="md-layout-item">
              <md-field>
                <label for="callee">Принимающая сторона (Callee)</label>
                <md-select v-model="callee" name="callee" id="callee">
                  <md-option value="kz">Казахстан (kz)</md-option>
                  <md-option value="ru">Россия (ru)</md-option>
                  <md-option value="de">Германия (de)</md-option>
                  <md-option value="gus">США (us)</md-option>
                </md-select>
              </md-field>
            </div>
          </div>
          <div class="flex flex-col">
            <md-checkbox v-model="all">Все </md-checkbox>
            <md-checkbox v-model="direct">Прямое соединение</md-checkbox>
            <md-checkbox v-model="additionalFirstNode"
              >Один дополнительный узел
            </md-checkbox>
            <md-checkbox v-model="additionalSecondNode">
              Два дополнительных узла
            </md-checkbox>
          </div>
        </md-card-content>
      </md-card>
    </form>
  </div>
</template>

<script>
export default {
  name: "searchForm",
  data() {
    return {
      caller: "kz",
      callee: "ru",
      all: false,
      direct: false,
      additionalFirstNode: false,
      additionalSecondNode: false,
    };
  },
};
</script>
