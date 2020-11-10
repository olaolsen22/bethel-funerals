<template lang="pug">
    div
        h2(v-html="content.heading")
        p(v-html="content.content")
        .special-box
            span I am planning my prepaid funeral
        form
            .form-group(v-for="(field, index) in content.fields")
                label(
                    :for="`enquire-field-${index}`" 
                    :class="{ required: field.required }"
                ) {{field.label}}
                input.form-control(
                    :type="field.type" 
                    :id="`enquire-field-${index}`" 
                    :placeholder="field.placeholder"
                )
            button.btn.btn-outline-light.mt-3(
                @click.prevent=""
                data-toggle="modal"
                data-target="#enquireNowModal"
            ) Submit
</template>

<script>
export default {
    props: {
        content: {
            type: Object,
            required: true
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../../assets/styles/variables.scss';

.form-group {
    display: flex;
    align-items: center;
    text-align: left;
    label { 
        width: 150px;
        margin-bottom: 0;
    }
    input {
        &.form-control {
            border: 0;
            border-radius: 0 !important;
        }
    }
}
.special-box {
    background-color: #FFFFFF;
    padding: .5rem 1rem;
    margin-bottom: 1.25rem;
    span {
        font-weight: bold;
        color: $primary;
    }
}
</style>