<script setup>
    import Feature from './Feature.vue';
</script>

<script>
    export default {
        data() {
            return {
                currentTab: 'Simple Bookmarking',
                tabs: ['Simple Bookmarking', 'Speedy Searching', 'Easy Sharing'],
                features: [
                    {
                        name: 'Simple Bookmarking',
                        heading: 'Bookmark in one click',
                        mainContent: `Organize your bookmarks however you like. Our simple drag-and-drop interface 
                            gives you complete control over how you manage your favourite sites.`,
                    },
                    {
                        name: 'Speedy Searching',
                        heading: 'Intelligent search',
                        mainContent: `Our powerful search feature will help you find saved sites in no time at all. 
                            No need to trawl through all of your bookmarks.`,
                    },
                    {
                        name: 'Easy Sharing',
                        heading: 'Share your bookmarks',
                        mainContent: `Easily share your bookmarks and collections with others. Create a shareable 
                            link that you can send at the click of a button.`,
                    },
                    
                ],
                currentTabInfo: {
                    heading: 'Bookmark in one click',
                    mainContent: `Organize your bookmarks however you like. Our simple drag-and-drop interface 
                            gives you complete control over how you manage your favourite sites.`,
                }
            }
        },
        methods: {
            changeTab(tab) {
                this.currentTab = tab;
                this.setCurrentTabInfo(tab);
            },
            setCurrentTabInfo(tab) {
                const currentTab = this.features.filter((value) => {
                    return value.name === tab
                })[0];
                this.currentTabInfo = {
                    heading: currentTab.heading,
                    mainContent: currentTab.mainContent,
                }
            }
        }
    }
</script>

<template>
    <section class="features-wrapper">
        <article class="features-info">
            <h2 class="features-heading">Features</h2>
            <p>
                Our aim is to make it quick and easy for you to access your favourite websites. 
                Your bookmarks sync between your devices so you can access them on the go.
            </p>
        </article>
        <ul class="features-nav">
            <li 
                v-for="tab in tabs" 
                @click="changeTab(tab)"
                v-bind:class="['tab-button', { active: currentTab === tab }]"
            >
                <button>{{tab}}</button>
            </li>
        </ul>
        <Feature 
            :heading="this.currentTabInfo.heading" 
            :mainContent="this.currentTabInfo.mainContent" 
        />
    </section>
</template>

<style scoped lang="sass">
    @import "../input.sass"

    .features-wrapper 
        margin-top: 195px

        .features-info
            width: 730px
            margin: 0 auto
            
            p, h2 
                text-align: center
            
            p
                margin: 0 auto
                margin-top: $contentVerticalMargin
                font-size: $mainFontSize
                width: 532px
                color: $grayishBlue
                line-height: 20px
        
        .features-nav 
            position: relative
            margin: 0 auto
            margin-top: 80px
            display: flex
            width: 730px
            justify-content: space-between

            &::after
                position: absolute
                top: 50px
                content: ''
                width: 100%
                border-top: 1px solid $grayishBlue

            .active
                position: relative

            .active:after
                content: ''
                position: absolute
                top: 50px
                left: -30px
                width: calc(100% + 60px)
                border-top: 4px solid $softRed
                z-index: 2

            button
                font-size: $mainFontSize
                letter-spacing: 1px
                background-color: inherit
                padding-bottom: 40px
                box-sizing: border-box

                &:hover
                    color: $softRed


</style>