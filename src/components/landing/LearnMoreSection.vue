<template lang="pug">
    .learn-more-container
        .container
            h2.mb-4 Learn more about Pre-paid funerals
            p.learn-more-description Here are a few helpful resources you might find useful when considering a pre-paid funeral:
            .cards-group
                .card-container
                    img(src="@/assets/images/image-1.jpg")
                    p Pre-Paid Funeral Calculator
                .card-container
                    img(src="@/assets/images/image-2.jpg")
                    p Funeral Bonds vs. Funeral Insurance
                .card-container
                    img(src="@/assets/images/image-3.jpg")
                    p Pre-Paid Funerals vs. Funeral Bonds

</template>

<style lang="scss" scoped>
@import '../../assets/styles/_variables.scss';

.learn-more-container {
    padding: 6rem 0;
    background-color: #DFEFF6;
    @media screen and (max-width: 768px) { padding: 3rem 0; }
    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
}
.learn-more-description {
    width: 26rem;
}
.cards-group {
    display: flex;
    justify-content: space-around;
    width: 100%;
    margin-top: 4rem;
    @media screen and (max-width: 768px) { 
        flex-wrap: wrap; 
        margin-top: 2rem;
    }
    .card-container {
        margin-bottom: 1rem;
        img {
            width: 300px;
            height: 218px;
        }
        p {
            width: 300px;
            margin-top: 1rem;
            font-weight: bold;
            text-transform: uppercase;
            text-align: left;
        }
        &:hover {
            cursor: pointer;
            color: $primary;
            text-decoration: underline;
        }
        &:last-child {
            p { margin-bottom: 0; }
        }
    }
}
</style>