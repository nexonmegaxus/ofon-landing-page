<template>
    <main>
        <section class="section fixed z-50 bg-[#F6F7F8] py-[8px] shadow-xl">
            <div class="div flex-row items-center justify-between">
                <div class="flex gap-[16px]">
                    <p class="font-14 font-semibold text-c-orange">{{ $t('c_navbar_1') }}</p>
                    <p class="font-14 font-semibold text-c-orange">{{ $t('c_navbar_2') }}</p>
                </div>
                <div class="flex gap-[16px]">
                    <div class="flex items-center gap-[10px]">
                        <img class="rounded-full" src="/img/en.webp" alt="Image" />
                        <NuxtLink :to="switchLocalePath('en')" class="font-14 font-semibold text-c-orange">EN</NuxtLink>
                    </div>
                    <div class="flex items-center gap-[10px]">
                        <img class="rounded-full" src="/img/id.webp" alt="Image" />
                        <NuxtLink :to="switchLocalePath('id')" class="font-14 font-semibold text-c-orange">ID</NuxtLink>
                    </div>
                </div>
            </div>
        </section>
        <section
            class="section fixed top-[36px] z-50 flex w-full flex-wrap border-b-2 border-[#eee] bg-white py-1 text-sm sm:flex-nowrap sm:justify-start sm:py-1"
        >
            <div class="mx-auto w-full px-[16px] py-[8px] sm:max-xl:max-w-[640px] xl:max-w-[1440px] xl:px-[120px] xl:py-[16px]">
                <div class="relative xl:flex xl:items-center">
                    <!-- 1 -->
                    <div class="flex items-center justify-between">
                        <!-- LOGO -->
                        <NuxtLink :to="localePath('/')"><img src="/img/ofon.webp" alt="Image" /></NuxtLink>
                        <div class="xl:hidden">
                            <button
                                type="button"
                                class="hs-collapse-toggle inline-flex items-center justify-center gap-x-2 rounded-lg border border-gray-200 bg-white p-2 text-gray-800 shadow-sm hover:bg-gray-50 focus:bg-gray-50 focus:outline-none disabled:pointer-events-none disabled:opacity-50"
                                id="hs-navbar-basic-usage-collapse"
                                aria-expanded="false"
                                aria-controls="hs-navbar-basic-usage"
                                aria-label="Toggle navigation"
                                data-hs-collapse="#hs-navbar-basic-usage"
                            >
                                <svg
                                    class="size-4 shrink-0 hs-collapse-open:hidden"
                                    xmlns="http://www.w3.org/2000/svg"
                                    width="24"
                                    height="24"
                                    viewBox="0 0 24 24"
                                    fill="none"
                                    stroke="currentColor"
                                    stroke-width="2"
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                >
                                    <line x1="3" x2="21" y1="6" y2="6" />
                                    <line x1="3" x2="21" y1="12" y2="12" />
                                    <line x1="3" x2="21" y1="18" y2="18" />
                                </svg>
                                <svg
                                    class="hidden size-4 shrink-0 hs-collapse-open:block"
                                    xmlns="http://www.w3.org/2000/svg"
                                    width="24"
                                    height="24"
                                    viewBox="0 0 24 24"
                                    fill="none"
                                    stroke="currentColor"
                                    stroke-width="2"
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                >
                                    <path d="M18 6 6 18" />
                                    <path d="m6 6 12 12" />
                                </svg>
                            </button>
                        </div>
                    </div>
                    <!-- 2 -->
                    <div
                        id="hs-navbar-basic-usage"
                        class="hs-collapse hidden grow basis-full overflow-hidden transition-all duration-300 xl:block"
                        aria-labelledby="hs-navbar-basic-usage-collapse"
                    >
                        <div
                            class="mt-5 flex flex-col gap-y-3 xl:mt-0 xl:flex-row xl:items-center xl:justify-end xl:gap-[10px] xl:gap-y-0 xl:ps-5"
                        >
                            <!-- MEGA MENU: SOLUTION -->
                            <div
                                class="hs-dropdown [--adaptive:none] [--is-collapse:true] [--strategy:static] sm:[--is-collapse:false] sm:[--strategy:absolute] sm:[--trigger:hover]"
                            >
                                <button
                                    id="hs-mega-menu"
                                    type="button"
                                    class="hs-dropdown-toggle font-12 flex w-full items-center font-semibold hover:text-c-orange sm:p-2"
                                    aria-haspopup="menu"
                                    aria-expanded="false"
                                    aria-label="Mega Menu"
                                >
                                    {{ $t('c_nav_1') }}
                                    <svg
                                        class="ml-1 size-4 shrink-0 duration-300 hs-dropdown-open:-rotate-180 sm:hs-dropdown-open:rotate-0"
                                        xmlns="http://www.w3.org/2000/svg"
                                        width="24"
                                        height="24"
                                        viewBox="0 0 24 24"
                                        fill="none"
                                        stroke="currentColor"
                                        stroke-width="2"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                    >
                                        <path d="m6 9 6 6 6-6" />
                                    </svg>
                                </button>

                                <div
                                    class="hs-dropdown-menu sm: start-0 z-10 hidden w-full min-w-60 rounded-lg border-[#eee] bg-white py-2 opacity-0 transition-[height] duration-300 ease-in-out before:absolute hs-dropdown-open:opacity-100 sm:px-2 sm:shadow-md sm:transition-[opacity,margin] sm:duration-[150ms] xl:top-[36px] xl:border xl:p-[16px]"
                                    role="menu"
                                    aria-orientation="vertical"
                                    aria-labelledby="hs-mega-menu"
                                >
                                    <div class="grid gap-[8px] sm:grid sm:grid-cols-3">
                                        <div class="flex flex-col">
                                            <p class="font-12 p-[4px] font-bold xl:p-[8px]">{{ $t('c_nav_2') }}</p>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/service/pbx-maintenance-service-support')"
                                                >{{ $t('c_nav_3') }}
                                            </NuxtLink>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/service/cloud-pbx-installation')"
                                                >{{ $t('c_nav_4') }}</NuxtLink
                                            >
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/service/phone-system-integration')"
                                                >{{ $t('c_nav_5') }}</NuxtLink
                                            >
                                        </div>
                                        <div class="flex flex-col">
                                            <p class="font-12 p-[4px] font-bold xl:p-[8px]">{{ $t('c_nav_6') }}</p>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/product/telephone')"
                                                >{{ $t('c_nav_7') }}
                                            </NuxtLink>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/product/internet')"
                                                >{{ $t('c_nav_8') }}</NuxtLink
                                            >
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/product/sip-trunk')"
                                                >{{ $t('c_nav_9') }}</NuxtLink
                                            >
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/product/meeting-setup')"
                                                >{{ $t('c_nav_10') }}</NuxtLink
                                            >
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/product/cloud-pbx')"
                                                >{{ $t('c_nav_11') }}</NuxtLink
                                            >
                                        </div>
                                        <div class="flex flex-col">
                                            <p class="font-12 p-[4px] font-bold xl:p-[8px]">{{ $t('c_nav_12') }}</p>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/use-case/maintain-legacy-phone-system')"
                                                >{{ $t('c_nav_13') }}
                                            </NuxtLink>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/use-case/migrate-on-premise')"
                                                >{{ $t('c_nav_14') }}</NuxtLink
                                            >
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/use-case/integrate-all-communication')"
                                                >{{ $t('c_nav_15') }}</NuxtLink
                                            >
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <!-- MEGA MENU: INDUSTRIES -->
                            <div
                                class="hs-dropdown [--adaptive:none] [--is-collapse:true] [--strategy:static] sm:[--is-collapse:false] sm:[--strategy:absolute] sm:[--trigger:hover]"
                            >
                                <button
                                    id="hs-mega-menu"
                                    type="button"
                                    class="hs-dropdown-toggle font-12 flex w-full items-center font-semibold hover:text-c-orange sm:p-2"
                                    aria-haspopup="menu"
                                    aria-expanded="false"
                                    aria-label="Mega Menu"
                                >
                                    {{ $t('c_nav_16') }}
                                    <svg
                                        class="ml-1 size-4 shrink-0 duration-300 hs-dropdown-open:-rotate-180 sm:hs-dropdown-open:rotate-0"
                                        xmlns="http://www.w3.org/2000/svg"
                                        width="24"
                                        height="24"
                                        viewBox="0 0 24 24"
                                        fill="none"
                                        stroke="currentColor"
                                        stroke-width="2"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                    >
                                        <path d="m6 9 6 6 6-6" />
                                    </svg>
                                </button>

                                <div
                                    class="hs-dropdown-menu sm: start-0 z-10 hidden w-fit min-w-60 rounded-lg border-[#eee] bg-white py-2 opacity-0 transition-[height] duration-300 ease-in-out before:absolute hs-dropdown-open:opacity-100 sm:px-2 sm:shadow-md sm:transition-[opacity,margin] sm:duration-[150ms] xl:left-[43%] xl:top-[36px] xl:border xl:p-[16px]"
                                    role="menu"
                                    aria-orientation="vertical"
                                    aria-labelledby="hs-mega-menu"
                                >
                                    <div class="grid gap-[8px] sm:grid sm:grid-cols-1">
                                        <div class="flex flex-col">
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/industry/finance')"
                                                >{{ $t('c_nav_17') }}
                                            </NuxtLink>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/industry/manufacturing')"
                                                >{{ $t('c_nav_18') }}
                                            </NuxtLink>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/industry/oil-and-gas')"
                                                >{{ $t('c_nav_19') }}
                                            </NuxtLink>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/industry/hospitality')"
                                                >{{ $t('c_nav_20') }}</NuxtLink
                                            >
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('/industry/healthcare')"
                                                >{{ $t('c_nav_21') }}</NuxtLink
                                            >
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <!-- MEGA MENU: SUCCESS STORIES -->
                            <div
                                class="hs-dropdown [--adaptive:none] [--is-collapse:true] [--strategy:static] sm:[--is-collapse:false] sm:[--strategy:absolute] sm:[--trigger:hover]"
                            >
                                <button
                                    id="hs-mega-menu"
                                    type="button"
                                    class="hs-dropdown-toggle font-12 flex w-full items-center font-semibold hover:text-c-orange sm:p-2"
                                    aria-haspopup="menu"
                                    aria-expanded="false"
                                    aria-label="Mega Menu"
                                >
                                    {{ $t('c_nav_22') }}
                                    <svg
                                        class="ml-1 size-4 shrink-0 duration-300 hs-dropdown-open:-rotate-180 sm:hs-dropdown-open:rotate-0"
                                        xmlns="http://www.w3.org/2000/svg"
                                        width="24"
                                        height="24"
                                        viewBox="0 0 24 24"
                                        fill="none"
                                        stroke="currentColor"
                                        stroke-width="2"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                    >
                                        <path d="m6 9 6 6 6-6" />
                                    </svg>
                                </button>

                                <div
                                    class="hs-dropdown-menu sm: start-0 z-10 hidden w-fit min-w-60 rounded-lg border-[#eee] bg-white py-2 opacity-0 transition-[height] duration-300 ease-in-out before:absolute hs-dropdown-open:opacity-100 sm:px-2 sm:shadow-md sm:transition-[opacity,margin] sm:duration-[150ms] xl:left-[55%] xl:top-[36px] xl:border xl:p-[16px]"
                                    role="menu"
                                    aria-orientation="vertical"
                                    aria-labelledby="hs-mega-menu"
                                >
                                    <div class="grid gap-[8px] sm:grid sm:grid-cols-1">
                                        <div class="flex flex-col">
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('case-study')"
                                                >{{ $t('c_nav_23') }}
                                            </NuxtLink>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('testimonial')"
                                                >{{ $t('c_nav_24') }}
                                            </NuxtLink>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <!-- MEGA MENU: RESOURCES -->
                            <div
                                class="hs-dropdown [--adaptive:none] [--is-collapse:true] [--strategy:static] sm:[--is-collapse:false] sm:[--strategy:absolute] sm:[--trigger:hover]"
                            >
                                <button
                                    id="hs-mega-menu"
                                    type="button"
                                    class="hs-dropdown-toggle font-12 flex w-full items-center font-semibold hover:text-c-orange sm:p-2"
                                    aria-haspopup="menu"
                                    aria-expanded="false"
                                    aria-label="Mega Menu"
                                >
                                    {{ $t('c_nav_25') }}
                                    <svg
                                        class="ml-1 size-4 shrink-0 duration-300 hs-dropdown-open:-rotate-180 sm:hs-dropdown-open:rotate-0"
                                        xmlns="http://www.w3.org/2000/svg"
                                        width="24"
                                        height="24"
                                        viewBox="0 0 24 24"
                                        fill="none"
                                        stroke="currentColor"
                                        stroke-width="2"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                    >
                                        <path d="m6 9 6 6 6-6" />
                                    </svg>
                                </button>

                                <div
                                    class="hs-dropdown-menu sm: start-0 z-10 hidden w-fit min-w-60 rounded-lg border-[#eee] bg-white py-2 opacity-0 transition-[height] duration-300 ease-in-out before:absolute hs-dropdown-open:opacity-100 sm:px-2 sm:shadow-md sm:transition-[opacity,margin] sm:duration-[150ms] xl:left-[67%] xl:top-[36px] xl:border xl:p-[16px]"
                                    role="menu"
                                    aria-orientation="vertical"
                                    aria-labelledby="hs-mega-menu"
                                >
                                    <div class="grid gap-[8px] sm:grid sm:grid-cols-1">
                                        <div class="flex flex-col">
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                to="/blog"
                                                >{{ $t('c_nav_26') }}
                                            </NuxtLink>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('calculators')"
                                                >{{ $t('c_nav_27') }}
                                            </NuxtLink>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <!-- MEGA MENU: ABOUT US -->
                            <div
                                class="hs-dropdown [--adaptive:none] [--is-collapse:true] [--strategy:static] sm:[--is-collapse:false] sm:[--strategy:absolute] sm:[--trigger:hover]"
                            >
                                <button
                                    id="hs-mega-menu"
                                    type="button"
                                    class="hs-dropdown-toggle font-12 flex w-full items-center font-semibold hover:text-c-orange sm:p-2"
                                    aria-haspopup="menu"
                                    aria-expanded="false"
                                    aria-label="Mega Menu"
                                >
                                    {{ $t('c_nav_28') }}
                                    <svg
                                        class="ml-1 size-4 shrink-0 duration-300 hs-dropdown-open:-rotate-180 sm:hs-dropdown-open:rotate-0"
                                        xmlns="http://www.w3.org/2000/svg"
                                        width="24"
                                        height="24"
                                        viewBox="0 0 24 24"
                                        fill="none"
                                        stroke="currentColor"
                                        stroke-width="2"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                    >
                                        <path d="m6 9 6 6 6-6" />
                                    </svg>
                                </button>

                                <div
                                    class="hs-dropdown-menu sm: start-0 z-10 hidden w-fit min-w-60 rounded-lg border-[#eee] bg-white py-2 opacity-0 transition-[height] duration-300 ease-in-out before:absolute hs-dropdown-open:opacity-100 sm:px-2 sm:shadow-md sm:transition-[opacity,margin] sm:duration-[150ms] xl:left-[76%] xl:top-[36px] xl:border xl:p-[16px]"
                                    role="menu"
                                    aria-orientation="vertical"
                                    aria-labelledby="hs-mega-menu"
                                >
                                    <div class="grid gap-[8px] sm:grid sm:grid-cols-1">
                                        <div class="flex flex-col">
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('about-us')"
                                                >{{ $t('c_nav_29') }}
                                            </NuxtLink>
                                            <NuxtLink
                                                class="font-12 rounded-lg p-[4px] font-medium hover:bg-[#eee] xl:p-[8px]"
                                                :to="localePath('gallery')"
                                                >{{ $t('c_nav_30') }}
                                            </NuxtLink>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <!-- CONTACT US -->
                            <NuxtLink id="contact-us" :to="localePath('contact-us')" class="btn font-12 text-white">{{
                                $t('c_navbar_3')
                            }}</NuxtLink>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <div class="h-[102px] xl:h-[119px]"></div>

        <!-- <div class="font-12 fixed flex flex-col bg-c-white opacity-80">
            <NuxtLink class="font-14 font-semibold" :to="localePath('/')">Home</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('about-us')">About Us</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('contact-us')">Contact Us</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('thank-you')">Thank You</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('solutions')">Solutions</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/solutions/migrate-on-premise-pbx-to-cloud-pbx')"
                >Solutions / Migrate On Premise</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/solutions/integrate-all-communication-channel')"
                >Solutions / Integrate Communication Channel</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/solutions/integrate-all-communication-device')"
                >Solutions / Integrate Communication Device</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('service')">Service</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/pbx-maintenance-service-support')"
                >Service / PBX Maintenance Support /
            </NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/pbx-maintenance-service-support/cisco')"
                >Service / PBX Maintenance Support / Cisco</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/pbx-maintenance-service-support/panasonic')"
                >Service / PBX Maintenance Support / Panasonic</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/pbx-maintenance-service-support/nec')"
                >Service / PBX Maintenance Support / NEC</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/pbx-maintenance-service-support/avaya')"
                >Service / PBX Maintenance Support / Avaya</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/pbx-maintenance-service-support/arcatel')"
                >Service / PBX Maintenance Support / Arcatel</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/cloud-pbx-installation')"
                >Service / Cloud PBX Installation</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/phone-system-integration')"
                >Service / Phone System Integration</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/phone-system-integration/microsoft-teams')"
                >Service / Phone System Integration / Microsoft Teams</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/phone-system-integration/cisco')"
                >Service / Phone System Integration / Cisco</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/service/phone-system-integration/zoom')"
                >Service / Phone System Integration / Zoom</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('industry')">Industry</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/industry/finance')">Industry / Finance</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/industry/manufacturing')"
                >Industry / Manufacturing</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/industry/hospitality')">Industry / Hospitality</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/industry/healthcare')">Industry / Healthcare</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('review')">Review</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('testimonial')">Testimonial</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('case-study')">Case Study</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/case-study/hospital')">Case Study / Hospital</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/case-study/oil-and-gas')"
                >Case Study / Oil And Gas</NuxtLink
            >
            <NuxtLink class="font-14 font-semibold" :to="localePath('/case-study/finance')">Case Study / Finance</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/case-study/banking')">Case Study / Banking</NuxtLink>
            <NuxtLink class="font-14 font-semibold" :to="localePath('/case-study/hospitality')"
                >Case Study / Hospitality</NuxtLink
            >
        </div> -->
    </main>
</template>

<script setup>
const localePath = useLocalePath();
const switchLocalePath = useSwitchLocalePath();
</script>

<style scoped>
#contact-us {
    color: white;
    text-decoration: none;
}

.router-link-exact-active {
    color: #f25921;
    text-decoration: underline;
    font-weight: 600;
}
</style>
