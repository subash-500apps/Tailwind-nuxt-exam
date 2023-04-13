<template>
  <div class="bg-white">
    <!-- Header -->
    <header class="absolute inset-x-0 top-0 z-50">
      <nav
        class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8"
        aria-label="Global"
      >
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Your Company</span>
            <img
              class="h-8 w-auto"
              height="36"
              width="170"
              src="https://recruithire.com/images/logo.svg?v=1681197388854523224"
              alt=""
            />
          </a>
        </div>
        <div class="flex lg:hidden">
          <button
            type="button"
            class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
            @click="mobileMenuOpen = true"
          >
            <span class="sr-only">Open main menu</span>
            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>

        <Menu as="div" class="relative inline-block text-left">
          <div>
            <MenuButton
              class="inline-flex w-full justify-center gap-x-1.5 rounded-md bg-white px-3 py-2 text-sm font-semibold text-gray-900 shadow-sm ring-inset ring-gray-300 hover:bg-gray-50"
            >
              Features
              <ChevronDownIcon
                class="-mr-1 h-5 w-5 text-gray-400"
                aria-hidden="true"
              />
            </MenuButton>
          </div>

          <transition
            enter-active-class="transition ease-out duration-100"
            enter-from-class="transform opacity-0 scale-95"
            enter-to-class="transform opacity-100 scale-100"
            leave-active-class="transition ease-in duration-75"
            leave-from-class="transform opacity-100 scale-100"
            leave-to-class="transform opacity-0 scale-95"
          >
            <MenuItems
              class="absolute right-0 z-10 mt-2 w-[50.0625rem] origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
            >
              <div class="py-1">
                <MenuItem v-slot="{ active }">
                  <a
                    href="#"
                    :class="[
                      active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                      'block px-4 py-2 text-sm',
                    ]"
                    >Candidate Management</a
                  >
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <a
                    href="#"
                    :class="[
                      active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                      'block px-4 py-2 text-sm',
                    ]"
                    >Resume Parsing</a
                  >
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <a
                    href="#"
                    :class="[
                      active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                      'block px-4 py-2 text-sm',
                    ]"
                    >Workflow Management</a
                  >
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <a
                    href="#"
                    :class="[
                      active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                      'block px-4 py-2 text-sm',
                    ]"
                    >Real-time Notifications</a
                  >
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <a
                    href="#"
                    :class="[
                      active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                      'block px-4 py-2 text-sm',
                    ]"
                    >Kanban Board</a
                  >
                </MenuItem>
                <form method="POST" action="#">
                  <MenuItem v-slot="{ active }">
                    <button
                      type="submit"
                      :class="[
                        active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                        'block w-full px-4 py-2 text-left text-sm',
                      ]"
                    >
                      Sign out
                    </button>
                  </MenuItem>
                </form>
              </div>
            </MenuItems>
          </transition>
        </Menu>
        <div class="p-2.5 text-sm font-semibold">
          <a href="https://recruithire.com/pricing">Pricing</a>
        </div>

        <Menu as="div" class="relative inline-block text-left">
          <div>
            <MenuButton
              class="inline-flex w-full justify-center gap-x-1.5 rounded-md bg-white px-3 py-2 text-sm font-semibold text-gray-900 shadow-sm ring-inset ring-gray-300 hover:bg-gray-50"
            >
              Resources
              <ChevronDownIcon
                class="-mr-1 h-5 w-5 text-gray-400"
                aria-hidden="true"
              />
            </MenuButton>
          </div>

          <transition
            enter-active-class="transition ease-out duration-100"
            enter-from-class="transform opacity-0 scale-95"
            enter-to-class="transform opacity-100 scale-100"
            leave-active-class="transition ease-in duration-75"
            leave-from-class="transform opacity-100 scale-100"
            leave-to-class="transform opacity-0 scale-95"
          >
            <MenuItems
              class="absolute right-0 z-10 mt-2 w-[50.0625rem] origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
            >
              <div class="py-1">
                <MenuItem v-slot="{ active }">
                  <a
                    href="#"
                    :class="[
                      active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                      'block px-4 py-2 text-sm',
                    ]"
                    >Applicant Tracking System</a
                  >
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <a
                    href="#"
                    :class="[
                      active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                      'block px-4 py-2 text-sm',
                    ]"
                    >Support</a
                  >
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <a
                    href="#"
                    :class="[
                      active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                      'block px-4 py-2 text-sm',
                    ]"
                    >License</a
                  >
                </MenuItem>
                <form method="POST" action="#">
                  <MenuItem v-slot="{ active }">
                    <button
                      type="submit"
                      :class="[
                        active ? 'bg-gray-100 text-gray-900' : 'text-gray-700',
                        'block w-full px-4 py-2 text-left text-sm',
                      ]"
                    >
                      Sign out
                    </button>
                  </MenuItem>
                </form>
              </div>
            </MenuItems>
          </transition>
        </Menu>
        <div class="hidden lg:flex lg:justify-end">
          <a href="#" class="text-sm font-semibold leading-6 text-gray-900"
            >Log In
          </a>
        </div>
        <div class="hidden lg:flex lg:justify-end p-6">
          <button
            type="button"
            class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
          >
            Sign Up
          </button>
        </div>
      </nav>
    </header>

    <main class="isolate">
      <!-- Body section -->
      <div class="relative isolate -z-10">
        <div class="overflow-hidden">
          <div
            class="mx-auto max-w-7xl px-6 pb-32 pt-36 sm:pt-60 lg:px-8 lg:pt-32"
          >
            <div
              class="mx-auto max-w-2xl gap-x-14 lg:mx-0 lg:flex lg:max-w-none lg:items-center"
            >
              <div class="w-full max-w-xl lg:shrink-0 xl:max-w-2xl">
                <h1
                  class="text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl"
                >
                  Applicant Tracking System
                </h1>
                <p color="bg-" class="text-3xl font-bold mt-6 text-blue-600">
                  Join the SaaS Revolution - 50 Apps for
                  <span class="pricing-id"> $999</span>
                </p>
                <div v-for="point in keypoints" :key="point.id">
                  <div class="flex mt-5">
                    <div class="mr-4"><CheckIcon class="h-5 w-5" /></div>
                    <div>
                      <span class="mt-6">{{ point.name }}</span>
                    </div>
                  </div>
                </div>
                <!--Footer section-->
                <div class="flex">
                  <div>
                    <button
                      type="button"
                      class="mt-10 rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
                    >
                      Sign Up
                      <div>14-day Trail</div>
                    </button>
                  </div>
                  <div class="mt-14 ml-3">
                    or
                    <img
                      src="https://recruithire.com/lib/images/sso-icons/google.svg?v=1681197388854523224"
                      alt="google"
                      width="30"
                      height="30"
                      class="ml-6 mt-[-1.5rem] google-icon-btn"
                    />
                  </div>
                  <img
                    src="https://recruithire.com/lib/images/sso-icons/linkedin.svg?v=1681197388854523224"
                    alt="LinkedIn"
                    class="ml-4 mt-10 linkedin-icon-btn"
                  />
                  <img
                    src="https://recruithire.com/lib/images/sso-icons/microsoft.svg?v=1681197388854523224"
                    alt="microsoft"
                    width="30"
                    height="30"
                    class="microsoft-icon-btn ml-6 mt-10"
                  />
                  <img
                    src="https://recruithire.com/lib/images/sso-icons/facebook.svg?v=1681197388854523224"
                    alt="Facebook"
                    width="30"
                    height="30"
                    class="facebook-icon-btn ml-6 mt-10"
                  />
                </div>
              </div>
              <div class="text-right">
                <object
                  class="mt-3"
                  data="https://recruithire.com/images/applicant-tracking-system.svg?v=1681197388854523224"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
import { defineComponent, h, ref } from "vue";
import { Bars3Icon } from "@heroicons/vue/24/outline";
import { Menu, MenuButton, MenuItem, MenuItems } from "@headlessui/vue";
import { ChevronDownIcon, CheckIcon } from "@heroicons/vue/20/solid";

// Define const values
const keypoints = [
  {
    id: 1,
    name: "Shortlist, schedule, and interview candidates faster through all-in-one recruitment software",
    icon: CheckIcon,
  },
  {
    id: 2,
    name: "Hire the best talent with resume parser, email integration, career portal, and smart bots",
    icon: CheckIcon,
  },
  {
    id: 3,
    name: "Accelerate and streamline the hiring process",
    icon: CheckIcon,
  },
  {
    id: 4,
    name: "Integrate applications like HRSprout for easier employee tracking & management",
    icon: CheckIcon,
  },
  {
    id: 5,
    name: "Automate the hiring process by using the visual workflows",
    icon: CheckIcon,
  },
];
const mobileMenuOpen = ref(false);
</script>
