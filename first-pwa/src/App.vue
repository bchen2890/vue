<template>
    <q-layout view="lHh Lpr lFf">
        <q-page-container>
            <router-view />
        </q-page-container>
        <q-footer elevated class="bg-grey-8 text-white">
            <BottomNav></BottomNav>
        </q-footer>
    </q-layout>
</template>

<script>
    import { defineComponent, ref } from 'vue';
    import BottomNav from '@/components/BottomNav.vue'

    export default defineComponent({
        name: 'App',

        components: {
            BottomNav
        },

        setup() {
            const leftDrawerOpen = ref(false);

            return {
                leftDrawerOpen,
                toggleLeftDrawer() {
                    leftDrawerOpen.value = !leftDrawerOpen.value;
                }
            };
        }
    })
</script>
