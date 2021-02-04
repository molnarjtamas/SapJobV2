<template>
<!--    <div class="relative flex items-top justify-center min-h-screen bg-gray-100 dark:bg-gray-900 sm:items-center sm:pt-0">-->
<!--        <div v-if="canLogin" class="hidden fixed top-0 right-0 px-6 py-4 sm:block">-->
<!--            <inertia-link v-if="$page.props.user" href="/dashboard" class="text-sm text-gray-700 underline">-->
<!--                Dashboard-->
<!--            </inertia-link>-->

<!--            <template v-else>-->
<!--                <inertia-link :href="route('login')" class="text-sm text-gray-700 underline">-->
<!--                    Login-->
<!--                </inertia-link>-->

<!--                <inertia-link v-if="canRegister" :href="route('register')" class="ml-4 text-sm text-gray-700 underline">-->
<!--                    Register-->
<!--                </inertia-link>-->
<!--            </template>-->
<!--        </div>-->

        <div class="container mx-auto flex justify-center md:flex-row items-center my-12 md:my-24">
            <!--Left Col-->
            <div class="flex flex-col w-full lg:w-1/2 justify-center items-start pt-12 pb-24 px-6">
                <p class="uppercase tracking-loose">If opportunity doesn't knock, build a door.</p>
                <h1 class="font-bold text-8xl my-4 text-green-800">SapJob</h1>
                <p class="leading-normal mb-4">We help students, fresh graduates and businesses grow by providing a platform ,where everyone can find a match for their talents and demands. Join our community and find the best opportunities! </p>
<!--                <button class="bg-transparent hover:bg-green-800 text-gray-900 hover:text-white rounded shadow hover:shadow-lg py-2 px-4 border border-gray-900 hover:border-transparent">Super Button</button>-->
                <div v-if="canLogin"  class="flex justify-end">

                    <jet-button  v-if="$page.props.user"  class="ml-4" >
                        <inertia-link  href="/dashboard" >
                            Go to site
                        </inertia-link>
                    </jet-button>

                    <template v-else>

                        <jet-button class="ml-4" >
                            <inertia-link :href="route('login')">
                                Login alma
                            </inertia-link>
                        </jet-button>

                        <jet-button class="ml-4" >
                        <inertia-link v-if="canRegister" :href="route('register')" >
                            Register
                        </inertia-link>
                        </jet-button>
                    </template>
            </div>
            </div>
            <!--Right Col-->
            <div class="w-full lg:w-1/2 lg:py-6 flex justify-end">
                <!--Add your product image here-->
<!--                <svg class="fill-current text-gray-900 w-3/5 mx-auto" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M17 6V5h-2V2H3v14h5v4h3.25H11a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6zm-5.75 14H3a2 2 0 0 1-2-2V2c0-1.1.9-2 2-2h12a2 2 0 0 1 2 2v4a2 2 0 0 1 2 2v10a2 2 0 0 1-2 2h-5.75zM11 8v8h6V8h-6zm3 11a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"/></svg>-->
                <jet-application-mark class=" h-auto w-3/5" />
            </div>

        </div>





</template>

<style scoped>
    .bg-gray-100 {
        background-color: #f7fafc;
        background-color: rgba(247, 250, 252, var(--tw-bg-opacity));
    }

    .border-gray-200 {
        border-color: #edf2f7;
        border-color: rgba(237, 242, 247, var(--tw-border-opacity));
    }

    .text-gray-400 {
        color: #cbd5e0;
        color: rgba(203, 213, 224, var(--tw-text-opacity));
    }

    .text-gray-500 {
        color: #a0aec0;
        color: rgba(160, 174, 192, var(--tw-text-opacity));
    }

    .text-gray-600 {
        color: #718096;
        color: rgba(113, 128, 150, var(--tw-text-opacity));
    }

    .text-gray-700 {
        color: #4a5568;
        color: rgba(74, 85, 104, var(--tw-text-opacity));
    }

    .text-gray-900 {
        color: #1a202c;
        color: rgba(26, 32, 44, var(--tw-text-opacity));
    }

    @media (prefers-color-scheme: dark) {
        .dark\:bg-gray-800 {
            background-color: #2d3748;
            background-color: rgba(45, 55, 72, var(--tw-bg-opacity));
        }

        .dark\:bg-gray-900 {
            background-color: #1a202c;
            background-color: rgba(26, 32, 44, var(--tw-bg-opacity));
        }

        .dark\:border-gray-700 {
            border-color: #4a5568;
            border-color: rgba(74, 85, 104, var(--tw-border-opacity));
        }

        .dark\:text-white {
            color: #fff;
            color: rgba(255, 255, 255, var(--tw-text-opacity));
        }

        .dark\:text-gray-400 {
            color: #cbd5e0;
            color: rgba(203, 213, 224, var(--tw-text-opacity));
        }
    }
</style>

<script>
    import JetApplicationLogo from "@/Jetstream/ApplicationLogo";
    import JetApplicationMark from '@/Jetstream/ApplicationMark';
    import JetButton from '@/Jetstream/Button';

    export default {
        components:{
            JetApplicationLogo,
            JetApplicationMark,
            JetButton
        },
        props: {
            canLogin: Boolean,
            canRegister: Boolean,
            laravelVersion: String,
            phpVersion: String,
        }
    }
</script>
