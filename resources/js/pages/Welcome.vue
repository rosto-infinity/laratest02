<script setup lang="ts">
import { Head, Link } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Welcome">
        <link rel="preconnect" href="https://rsms.me/" />
        <link rel="stylesheet" href="https://rsms.me/inter/inter.css" />
    </Head>
    <div class="flex min-h-screen flex-col items-center bg-[#FDFDFC] p-6 text-[#1b1b18] dark:bg-[#0a0a0a] lg:justify-center lg:p-8">
        <header class="not-has-[nav]:hidden mb-6 w-full max-w-[335px] text-sm lg:max-w-4xl">
            <nav class="flex items-center justify-end gap-4">
                <Link
                    v-if="$page.props.auth.user"
                    :href="route('dashboard')"
                    class="inline-block rounded-sm border border-[#19140035] px-5 py-1.5 text-sm leading-normal text-[#1b1b18] hover:border-[#1915014a] dark:border-[#3E3E3A] dark:text-[#EDEDEC] dark:hover:border-[#62605b]"
                >
                    Dashboard
                </Link>
                <template v-else>
                    <Link
                        :href="route('login')"
                        class="inline-block rounded-sm border border-transparent px-5 py-1.5 text-sm leading-normal text-[#1b1b18] hover:border-[#19140035] dark:text-[#EDEDEC] dark:hover:border-[#3E3E3A]"
                    >
                        Log in
                    </Link>
                    <Link
                        :href="route('register')"
                        class="inline-block rounded-sm border border-[#19140035] px-5 py-1.5 text-sm leading-normal text-[#1b1b18] hover:border-[#1915014a] dark:border-[#3E3E3A] dark:text-[#EDEDEC] dark:hover:border-[#62605b]"
                    >
                        Register
                    </Link>
                </template>
            </nav>
        </header>
        <div
            class="duration-750 starting:opacity-0 flex w-full items-center justify-center opacity-100 transition-opacity lg:grow">
            <div class="bg-gray-100 py-8">
                <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
                    <h1 class="text-4xl text-green-600 pb-4">Prof rostand lele</h1>
                    <h2 class="text-3xl font-bold text-gray-800 mb-6">La stack VITL</h2>
                    <div class="space-y-6">
                        <div>
                            <h3 class="text-xl font-bold text-gray-800 mb-2">Vue.js</h3>
                            <p class="text-gray-600">Vue.js est un framework JavaScript pour la construction
                                d'interfaces
                                utilisateur. Il offre une expérience de développement agréable et des performances
                                optimales.
                            </p>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold text-gray-800 mb-2">Inertia.js</h3>
                            <p class="text-gray-600">Inertia.js est un framework qui permet de créer des applications
                                web
                                monopage (SPA) en utilisant des frameworks côté serveur comme Laravel. Cela permet de
                                garder une
                                architecture serveur traditionnelle tout en offrant une expérience utilisateur fluide.
                            </p>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold text-gray-800 mb-2">Tailwind CSS</h3>
                            <p class="text-gray-600">Tailwind CSS est un framework CSS utilitaire qui accélère le
                                développement
                                front-end en fournissant une grande variété de classes CSS prédéfinies.</p>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold text-gray-800 mb-2">Laravel</h3>
                            <p class="text-gray-600">Laravel est un framework PHP populaire qui apporte une solide
                                architecture
                                serveur avec de nombreuses fonctionnalités telles que la gestion des routes, la
                                connexion à la
                                base de données, la gestion des sessions, etc.</p>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold text-gray-800 mb-2">Pourquoi la stack VITL ?</h3>
                            <p class="text-gray-600">Cette stack "VITL" combine donc les forces de chacun de ces outils
                                :</p>
                            <ul class="list-disc pl-6 text-gray-600">
                                <li>Vue.js pour une expérience de développement agréable et des performances optimales
                                </li>
                                <li>Inertia.js pour une expérience utilisateur fluide et réactive</li>
                                <li>Tailwind CSS pour accélérer le développement front-end</li>
                                <li>Laravel pour une architecture serveur robuste</li>
                            </ul>
                            <p class="text-gray-600">Cela en fait une stack particulièrement adaptée pour le
                                développement
                                d'applications web modernes, offrant à la fois une bonne productivité de développement
                                et une
                                architecture serveur traditionnelle.</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>
        <div class="h-14.5 hidden lg:block"></div>
    </div>
</template>
