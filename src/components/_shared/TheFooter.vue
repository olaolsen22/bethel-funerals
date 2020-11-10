<template lang="pug">
    .the-header
        .container
            .the-footer-content
                .left-nav
                    a.nav-text.link(href="") Contact Us
                    span.nav-text.spacer /
                    a.nav-text.link(href="") Privacy Policy
                .nav-text.copyright © Bethel Funerals. All rights reserved.
</template>

<style lang="scss" scoped>
@import '../../assets/styles/variables.scss';

.the-header {
    background-color: white;
    width: 100%;
    .main-logo {
        height: 3rem;
        width: auto;
        @media screen and (max-width: 420px) { height: 2rem; }
    }
    .the-footer-content {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        height: 6rem;
        @media screen and (max-width: 420px) { 
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
    }
}
.left-nav {
    display: flex;
    align-items: center;
    a {
        height: 2rem;
        display: flex;
        align-items: center;
    }
}
.nav-text {
    color: $primary;
    font-size: 14px;
    font-weight: bold;
    &.spacer { margin: 0 .5rem; }
    &.link {
        height: 2rem;
        &:hover { text-decoration: underline;}
    }
    &.copyright { font-weight: normal; }
    @media screen and (max-width: 420px) { 
        font-size: 14px;
        text-align: left;
        &.spacer { margin: 0 .5rem; }
        &.copyright { padding: .5rem 0 }
    }
}
</style>