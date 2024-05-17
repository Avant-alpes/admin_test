<template>
    <div id="divLogo">
        <div id="subDivLogo" @mouseover="changeLogo" >
            <img :src="currentLogo" alt="Vue logo" id="logo">
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            logos: [
                require('../assets/logo-avantalpes-blanc-cmjn-fondnoir.svg'),
                require('../assets/logo-avantalpes-noir-cmjn-fondblanc.svg'),
            ],
            currentLogoIndex: 0,
        };
    },
    computed: {
        currentLogo() {
            return this.logos[this.currentLogoIndex];
        }
    },
    methods: {
        changeLogo() {
            this.currentLogoIndex = (this.currentLogoIndex + 1) % this.logos.length;
        }
    }
};
</script>

<style scoped>
#divLogo {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 300px;
}

#subDivLogo {
    width: 300px;
    height: 300px;
    cursor: pointer;
}

#logo {
    width: 9000px;
    height: 300px;
    cursor: pointer;
}
</style>