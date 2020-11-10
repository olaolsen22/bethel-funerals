<template lang="pug">
    .the-header
        .container
            .the-header-content
                img.main-logo(src="@/assets/logo.png")
                a.phone-link(href="tel:(03) 9873 8866") (03) 9873 8866
</template>

<style lang="scss" scoped>
@import '../../assets/styles/variables.scss';

.the-header {
    background-color: white;
    width: 100%;
    .main-logo {
        height: 3rem;
        width: auto;
        @media screen and (max-width: 512px) { height: 2rem; }
    }
    .the-header-content {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        height: 8rem;
        @media screen and (max-width: 512px) { height: 4rem; }
    }
}
.phone-link {
    color: $primary;
    font-weight: bold;
    &:hover {
        text-decoration: underline;
    }
    @media screen and (max-width: 512px) { font-size: .75rem; }
}
</style>