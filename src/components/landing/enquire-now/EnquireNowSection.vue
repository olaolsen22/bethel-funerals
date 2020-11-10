<template lang="pug">
    .enquire-now-container
        .container
            .modal.fade(tabindex="-1" role="dialog" id="enquireNowModal")
                .modal-dialog.modal-fullscreen(role="document")
                    .modal-content
                        button.close(
                            type="button"
                            data-dismiss="modal"
                            aria-label="Close"
                        ) &times;
                        EnquireNowForm(:content="rightPane")
            .row
                .col-12.col-md-6.pane
                    h2(v-html="leftPane.heading")
                    p(v-html="leftPane.content")
                    button.btn.btn-outline-light.inverted.mx-auto.d-block.d-md-none(
                        type="button"
                        data-toggle="modal"
                        data-target="#enquireNowModal"
                    ) Enquire Now
                .col-6.pane.d-none.d-md-block
                    EnquireNowForm(:content="rightPane")
</template>

<script>
import EnquireNowForm from './EnquireNowForm.vue'

export default {
    components: {
        EnquireNowForm
    },
    data () {
        return {
            leftPane: {
                heading: 'Arrange a pre-paid funeral with Bethel before *31st March 2020 and we’ll waive our $275 administration fee.<br/><br/>',
                content: 'So, not only will you save money today, you’ll also benefit from having your funeral costs fixed at today’s prices – saving  your family the financial costs of a funeral in the future.<br/><br/>At Bethel Funerals we think the real value of a pre-paid funeral is peace of mind. You will have peace of mind knowing that your wishes will be thoughtfully carried out by our professional caring staff and you’ll have peace of mind knowing that your loved ones won’t need to find money to pay for the service when the time comes.'
            },
            rightPane: {
                heading: 'Enquire Now',
                content: 'Fill in the form below and one of our helpful staff will respond to you in the next 24 hours.',
                fields: [
                    { label: 'First Name', placeholder: 'Gordon', type: 'text', required: false },
                    { label: 'Last Name', placeholder: 'Pont', type: 'text', required: false },
                    { label: 'Email', placeholder: 'gordon@collabagency.com.au', type: 'email', required: true },
                    { label: 'Phone', placeholder: '0435 677 890', type: 'phone', required: false }
                ]
            }
        }
    },
    methods: {
        // createElementId (prefix, suffix) {

        // }
    }
}
</script>

<style lang="scss" scoped>
@import '../../../assets/styles/variables.scss';

.enquire-now-container {
    background: linear-gradient(90deg, #FFFFFF 50%, $primary 50%);
    padding: 6rem 0;
    @media screen and (max-width: 768px) { padding: 3rem 0; } 
    @media screen and (max-width: 767px) { background: #FFFFFF }
}
.pane {
    display: flex;
    flex-direction: column;
    text-align: left;
    padding-right: 4rem;
    &:last-child {
        padding-right: 0;
        padding-left: 4rem;
        color: #FFFFFF;
    }
    &:first-child {
        p { margin-bottom: 0; }
    }
    @media screen and (max-width: 768px) {
        padding-right: 2rem;
        &:last-child {
            padding-right: 0;
            padding-left: 2rem;
        }
    }
    @media screen and (max-width: 512px) { 
        text-align: center; 
        padding: 0 1.25rem;
    }
}
.modal-dialog{
    &.modal-fullscreen {
        margin: 0;
        width: 100vw;
        .modal-content {
            padding: 2rem;
            padding-top: 3rem;
            width: 100vw;
            height: 100vh;
            color: #FFFFFF;
            background-color: $primary !important;
            button {
                &.close {
                    position: absolute;
                    top: 1rem;
                    right: 1rem;
                    color: #FFFFFF;
                    font-size: 2rem;
                }
            }
        }
    }
}
</style>