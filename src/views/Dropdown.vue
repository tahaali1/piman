<template>
  <div>
    <section>
      <h2>下拉選單</h2>
      <article>
        <section>
          <h3>大小</h3>
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            size="small"
            @click="onClick"
            listboxClass="abc"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            size="large"
            @click="onClick"
          />
        </section>
        <section>
          <h3>客製化文字</h3>
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            @click="onClick"
          />
        </section>
        <section>
          <h3>前綴插槽</h3>
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            size="small"
            @click="onClick"
           >
            <template v-slot:prefix>前綴插槽</template>
            <template v-slot:affix>後綴插槽</template>
          </bpa-dropdown>
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            @click="onClick"
           >
            <template v-slot:prefix>
              <img src="favicon.ico" alt=""/>
            </template>
          </bpa-dropdown>
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            size="large"
            @click="onClick"
           >
            <template v-slot:prefix>
              <img src="favicon.ico" alt=""/>
            </template>
          </bpa-dropdown>
        </section>
        <section>
          <h3>顏色</h3>
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="primary"
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="success"
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="warning"
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="danger"
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="primary-ghost"
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="success-ghost"
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="warning-ghost"
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="danger-ghost"
            @click="onClick"
          />
        </section>
        <section>
          <h3>停用</h3>
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            disabled
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="primary"
            disabled
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="success"
            disabled
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="warning"
            disabled
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="danger"
            disabled
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="primary-ghost"
            disabled
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="success-ghost"
            disabled
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="warning-ghost"
            disabled
            @click="onClick"
          />
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            theme="danger-ghost"
            disabled
            @click="onClick"
          />
        </section>
        <section>
          <h3>客製化展開寬度</h3>
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            optionWidth="100px"
            @click="onClick"
          />
        </section>
        <section>
          <h3>若下拉選單位於 position: fixed; 位置裡時</h3>
          <bpa-dropdown
            v-model="value"
            :options="options"
            placeholder="執行動作"
            fixed
            @click="onClick"
          />
        </section>
      </article>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      value: '',
      options: [
        { type: 'link', url: '/', label: '<mark>內部連結</mark>', },
        { type: 'external-link', url: 'https://google.com', label: '外部連結' },
        { label: '功能按鈕', }
      ],
    }
  },
  methods: {
    onClick(item: any){
      console.log(item);
    }
  }
})
</script>

