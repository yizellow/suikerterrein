<script setup lang="ts">
const heroImages = [
  {
    src: '/images/hero-1.jpg',
    alt: 'Suikerterrein image 1',
    caption: 'Field research at Suikerterrein'
  },
  {
    src: '/images/hero-2.jpg',
    alt: 'Suikerterrein image 2',
    caption: 'Artist community and temporary spaces'
  },
  {
    src: '/images/hero-3.jpg',
    alt: 'Suikerterrein image 3',
    caption: 'Traces of cultural production'
  }
]

const navItems = [
  { label: 'Introduction', href: '#introduction' },
  { label: 'About Suikerterrein', href: '#about' },
  { label: 'Interviews', href: '#interviews' },
  { label: 'Team', href: '#team' }
]

const aboutSections = [
  {
    title: 'History',
    text: 'Placeholder text about the historical development of Suikerterrein, its former industrial use, and the gradual transition into a cultural and artistic site.'
  },
  {
    title: 'Current Use',
    text: 'Placeholder text about how artists, makers, cultural organizers, and visitors currently use the site for studios, events, experiments, and informal gathering.'
  },
  {
    title: 'Future Change',
    text: 'Placeholder text about expected redevelopment, uncertainty around the timeline, and the possible transformation or disappearance of existing cultural spaces.'
  },
  {
    title: 'Why It Matters',
    text: 'Placeholder text about the social, artistic, and civic value of temporary cultural places, and the questions that remain when they are removed.'
  }
]

const interviews = [
  {
    name: 'Maruschka & Laurens',
    image: '/images/interview-maruschka-laurens.jpg',
    description: 'Artists connected to Suikerterrein.',
    summary: 'Interview summary placeholder...',
    quote: 'Quote placeholder...',
    audio: '/audio/maruschka-laurens.mp3'
  },
  {
    name: 'Robert',
    image: '/images/interview-robert.jpg',
    description: 'Artist or cultural worker connected to the site.',
    summary: 'Interview summary placeholder...',
    quote: 'Quote placeholder...',
    audio: '/audio/robert.mp3'
  },
  {
    name: 'Floris',
    image: '/images/interview-floris.jpg',
    description: 'Artist or cultural worker connected to the site.',
    summary: 'Interview summary placeholder...',
    quote: 'Quote placeholder...',
    audio: '/audio/floris.mp3'
  }
]

const teamMembers = [
  {
    name: 'Name 1',
    image: '/images/team-1.jpg',
    bio: 'Short biography placeholder...',
    reflection: 'Personal reflection on the project placeholder...'
  },
  {
    name: 'Name 2',
    image: '/images/team-2.jpg',
    bio: 'Short biography placeholder...',
    reflection: 'Personal reflection on the project placeholder...'
  },
  {
    name: 'Name 3',
    image: '/images/team-3.jpg',
    bio: 'Short biography placeholder...',
    reflection: 'Personal reflection on the project placeholder...'
  },
  {
    name: 'Name 4',
    image: '/images/team-4.jpg',
    bio: 'Short biography placeholder...',
    reflection: 'Personal reflection on the project placeholder...'
  }
]

const currentHeroIndex = ref(0)
let heroInterval: ReturnType<typeof setInterval> | undefined

const currentHeroImage = computed(() => heroImages[currentHeroIndex.value])

const selectHeroImage = (index: number) => {
  currentHeroIndex.value = index
}

onMounted(() => {
  heroInterval = setInterval(() => {
    currentHeroIndex.value = (currentHeroIndex.value + 1) % heroImages.length
  }, 5000)
})

onBeforeUnmount(() => {
  if (heroInterval) {
    clearInterval(heroInterval)
  }
})
</script>

<template>
  <main class="min-h-screen bg-stone-50 text-neutral-900 antialiased">
    <section class="border-b border-neutral-300 bg-stone-100">
      <div class="mx-auto max-w-7xl px-4 py-5 sm:px-6 lg:px-8">
        <p class="text-xs uppercase tracking-[0.24em] text-neutral-500">
          Artist research / Field archive / Groningen
        </p>
      </div>

      <div class="mx-auto max-w-7xl px-4 pb-8 sm:px-6 lg:px-8">
        <div class="relative overflow-hidden border border-neutral-300 bg-neutral-200">
          <Transition name="fade" mode="out-in">
            <img
              :key="currentHeroImage.src"
              :src="currentHeroImage.src"
              :alt="currentHeroImage.alt"
              class="h-[62vh] min-h-[360px] w-full object-cover grayscale-[20%] sm:h-[68vh]"
            >
          </Transition>
        </div>

        <div class="mt-4 grid gap-4 border-b border-neutral-300 pb-6 md:grid-cols-[1fr_auto] md:items-end">
          <div>
            <h1 class="max-w-4xl text-4xl font-normal leading-tight text-neutral-950 sm:text-5xl lg:text-7xl">
              Suikerterrein
            </h1>
            <p class="mt-3 max-w-2xl text-base leading-7 text-neutral-700 sm:text-lg">
              {{ currentHeroImage.caption }}
            </p>
          </div>

          <div class="flex gap-2 overflow-x-auto pb-1 md:justify-end">
            <button
              v-for="(image, index) in heroImages"
              :key="image.src"
              type="button"
              class="group shrink-0 border bg-stone-50 p-1 transition duration-200"
              :class="currentHeroIndex === index ? 'border-neutral-900' : 'border-neutral-300 hover:border-neutral-600'"
              :aria-label="`Show ${image.alt}`"
              @click="selectHeroImage(index)"
            >
              <img
                :src="image.src"
                :alt="image.alt"
                class="h-16 w-24 object-cover grayscale transition duration-200 group-hover:grayscale-0 sm:h-20 sm:w-32"
                :class="currentHeroIndex === index ? 'grayscale-0' : ''"
              >
            </button>
          </div>
        </div>
      </div>
    </section>

    <nav class="sticky top-0 z-20 border-b border-neutral-300 bg-stone-50/95 backdrop-blur">
      <div class="mx-auto max-w-7xl overflow-x-auto px-4 sm:px-6 lg:px-8">
        <div class="flex min-w-max items-center gap-8 py-4 text-sm uppercase tracking-[0.18em] text-neutral-600">
          <a
            v-for="item in navItems"
            :key="item.href"
            :href="item.href"
            class="whitespace-nowrap transition duration-200 hover:text-neutral-950"
          >
            {{ item.label }}
          </a>
        </div>
      </div>
    </nav>

    <section id="introduction" class="scroll-mt-24 border-b border-neutral-300">
      <div class="mx-auto grid max-w-7xl gap-12 px-4 py-20 sm:px-6 md:grid-cols-[0.8fr_1.2fr] lg:px-8 lg:py-28">
        <div>
          <p class="text-xs uppercase tracking-[0.24em] text-neutral-500">
            Introduction
          </p>
          <h2 class="mt-4 text-3xl font-normal leading-tight text-neutral-950 sm:text-4xl">
            Artist Research: Suikerterrein
          </h2>
        </div>

        <div class="max-w-3xl text-lg leading-8 text-neutral-700">
          <p>
            This website presents an artist research project about Suikerterrein, an artist and cultural community in Groningen that is expected to disappear around 2030 due to future redevelopment. Through interviews, we investigated how artists experience this place, how they build community, and what may be lost when such temporary cultural spaces are removed.
          </p>
        </div>
      </div>
    </section>

    <section class="border-b border-neutral-300 bg-[#ede8df]">
      <div class="mx-auto grid max-w-7xl gap-12 px-4 py-20 sm:px-6 md:grid-cols-[0.8fr_1.2fr] lg:px-8 lg:py-28">
        <div>
          <p class="text-xs uppercase tracking-[0.24em] text-neutral-500">
            Research ground
          </p>
          <h2 class="mt-4 text-3xl font-normal leading-tight text-neutral-950 sm:text-4xl">
            Motivation
          </h2>
        </div>

        <div class="max-w-3xl text-lg leading-8 text-neutral-700">
          <p>
            Our motivation comes from a concern for temporary artist communities and the fragile spaces that support them. Suikerterrein is not only a physical location, but also a living network of artists, makers, events, memories, and informal support. By interviewing people connected to the site, we want to understand what this place means before it changes or disappears.
          </p>
        </div>
      </div>
    </section>

    <section id="about" class="scroll-mt-24 border-b border-neutral-300">
      <div class="mx-auto grid max-w-7xl gap-12 px-4 py-20 sm:px-6 md:grid-cols-[0.8fr_1.2fr] lg:px-8 lg:py-28">
        <div>
          <p class="text-xs uppercase tracking-[0.24em] text-neutral-500">
            Site notes
          </p>
          <h2 class="mt-4 text-3xl font-normal leading-tight text-neutral-950 sm:text-4xl">
            About Suikerterrein
          </h2>
          <p class="mt-5 max-w-sm text-sm leading-6 text-neutral-600">
            A compact archive of context, temporary use, future redevelopment, and the cultural questions around the site.
          </p>
        </div>

        <div class="grid gap-6 sm:grid-cols-2">
          <article
            v-for="section in aboutSections"
            :key="section.title"
            class="border border-neutral-300 bg-stone-50 p-6"
          >
            <h3 class="text-xl font-normal text-neutral-950">
              {{ section.title }}
            </h3>
            <p class="mt-4 text-base leading-7 text-neutral-700">
              {{ section.text }}
            </p>
          </article>
        </div>
      </div>
    </section>

    <section id="interviews" class="scroll-mt-24 border-b border-neutral-300 bg-[#342c25] text-stone-50">
      <div class="mx-auto max-w-7xl px-4 py-20 sm:px-6 lg:px-8 lg:py-28">
        <div class="grid gap-8 md:grid-cols-[0.8fr_1.2fr]">
          <div>
            <p class="text-xs uppercase tracking-[0.24em] text-stone-400">
              Oral archive
            </p>
            <h2 class="mt-4 text-3xl font-normal leading-tight sm:text-4xl">
              Interviews
            </h2>
          </div>

          <p class="max-w-3xl text-lg leading-8 text-stone-300">
            Interview fragments and summaries from people connected to Suikerterrein, gathered as part of an artist research process.
          </p>
        </div>

        <div class="mt-14 grid gap-6 lg:grid-cols-3">
          <article
            v-for="interview in interviews"
            :key="interview.name"
            class="flex flex-col border border-stone-600 bg-[#2b251f]"
          >
            <img
              :src="interview.image"
              :alt="`${interview.name} interview portrait`"
              class="aspect-[4/3] w-full object-cover grayscale-[25%]"
            >

            <div class="flex flex-1 flex-col p-6">
              <p class="text-xs uppercase tracking-[0.2em] text-stone-400">
                Interview
              </p>
              <h3 class="mt-3 text-2xl font-normal text-stone-50">
                {{ interview.name }}
              </h3>
              <p class="mt-3 text-sm leading-6 text-stone-300">
                {{ interview.description }}
              </p>
              <p class="mt-5 text-base leading-7 text-stone-200">
                {{ interview.summary }}
              </p>
              <blockquote class="mt-6 border-l border-stone-400 pl-4 text-base italic leading-7 text-stone-200">
                "{{ interview.quote }}"
              </blockquote>
              <audio class="mt-6 w-full" controls :src="interview.audio" />
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="team" class="scroll-mt-24 bg-stone-50">
      <div class="mx-auto max-w-7xl px-4 py-20 sm:px-6 lg:px-8 lg:py-28">
        <div class="grid gap-8 md:grid-cols-[0.8fr_1.2fr]">
          <div>
            <p class="text-xs uppercase tracking-[0.24em] text-neutral-500">
              Project group
            </p>
            <h2 class="mt-4 text-3xl font-normal leading-tight text-neutral-950 sm:text-4xl">
              Team
            </h2>
          </div>

          <p class="max-w-3xl text-lg leading-8 text-neutral-700">
            Short biographies and reflections from the research team, kept together as part of the project archive.
          </p>
        </div>

        <div class="mt-14 grid gap-6 sm:grid-cols-2 lg:grid-cols-4">
          <article
            v-for="member in teamMembers"
            :key="member.name"
            class="border border-neutral-300 bg-[#f6f2ea]"
          >
            <img
              :src="member.image"
              :alt="`${member.name} portrait`"
              class="aspect-[3/4] w-full object-cover grayscale-[20%]"
            >
            <div class="p-5">
              <h3 class="text-xl font-normal text-neutral-950">
                {{ member.name }}
              </h3>
              <p class="mt-3 text-sm leading-6 text-neutral-700">
                {{ member.bio }}
              </p>
              <p class="mt-5 border-t border-neutral-300 pt-4 text-sm leading-6 text-neutral-600">
                {{ member.reflection }}
              </p>
            </div>
          </article>
        </div>
      </div>
    </section>
  </main>
</template>
