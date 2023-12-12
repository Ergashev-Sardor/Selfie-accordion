<template>
  <div>
    <input :id="label" name="accordion-1" type="radio" :checked="isChecked"  @click="toggle"/>
    <label :for="label">{{ label }}</label>
    <article>
      <p>{{ content }} </p>
    </article>
  </div>
</template>

<script>
export default {
  name: "AccordionCard",
  props: {
    label: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    },
  },
  data: () => ({
    isChecked: false
  }),
  methods: {
    toggle() {
      this.isChecked = !this.isChecked
    }
  }
}
</script>

<style>

</style>