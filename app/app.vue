<script setup lang="ts">
const heroImages = [
  {
    src: '/images/hero-1.jpeg',
    alt: 'Suikerterrein image 1',
    caption: 'Field research at Suikerterrein'
  },
  {
    src: '/images/hero-2.jpeg',
    alt: 'Suikerterrein image 2',
    caption: 'Artist community and temporary spaces'
  },
  {
    src: '/images/hero-3.jpeg',
    alt: 'Suikerterrein image 3',
    caption: 'Traces of cultural production'
  },
  {
    src: '/images/hero-4.jpeg',
    alt: 'Suikerterrein image 4',
    caption: 'Industrial traces and everyday use'
  },
  {
    src: '/images/hero-5.jpeg',
    alt: 'Suikerterrein image 5',
    caption: 'Temporary cultural space in transition'
  },
  {
    src: '/images/hero-6.jpeg',
    alt: 'Suikerterrein image 6',
    caption: 'Field observation around the site'
  },
  {
    src: '/images/hero-7.jpeg',
    alt: 'Suikerterrein image 7',
    caption: 'Archive fragments from Suikerterrein'
  },
  {
    src: '/images/hero-8.jpeg',
    alt: 'Suikerterrein image 8',
    caption: 'Artistic community and urban change'
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
    title: 'About the Site',
    text: 'Suikerterrein is part of Groningen’s former sugar factory site. Once connected to the city’s industrial production, the area has gradually been reused after the factory closed. In recent years, it has developed into a mixed and transitional urban space that includes events, food, education, workshops, creative practices, and a wide range of users.'
  },
  {
    title: 'Why It Matters',
    text: 'The specificity of Suikerterrein lies in the fact that it is neither a fully planned new district nor simply a preserved industrial site. It remains a place in transition. Temporary use, open-ended development, and future urban redevelopment overlap here, making it an important case for observing how cities change.'
  },
  {
    title: 'Why We Study It',
    text: 'For our artist research, Suikerterrein is not only about which artists work here. We are interested in how artistic practice becomes embedded in a changing environment. Artist communities, event spaces, and other users together shape the site’s current cultural, spatial, and social condition.'
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
    name: 'Yize Isaac',
    role: 'Researcher / Artist',
    image: '/images/team-yize.jpg',
    bio: 'I am from Taipei, Taiwan. My practice begins with the body, vulnerability, memory, and states of survival.',
    reflection: 'For this project, I focus on Suikerterrein as a fragile cultural space where art, memory, and urban transformation intersect.'
  },
  {
    name: 'Name 2',
    role: 'Researcher',
    image: '/images/team-2.jpg',
    bio: 'Short biography placeholder for a team member involved in field research, interviews, and site observation.',
    reflection: 'Project reflection placeholder about the relationship between temporary cultural space, community, and urban change.'
  },
  {
    name: 'Name 3',
    role: 'Researcher',
    image: '/images/team-3.jpg',
    bio: 'Short biography placeholder for a team member contributing to documentation, analysis, and artistic research.',
    reflection: 'Project reflection placeholder about what can be learned from artists working in a changing environment.'
  },
  {
    name: 'Name 4',
    role: 'Researcher',
    image: '/images/team-4.jpg',
    bio: 'Short biography placeholder for a team member working with interview material and field notes.',
    reflection: 'Project reflection placeholder about memory, place, and the future of cultural communities.'
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
  <main class="min-h-screen bg-stone-50 text-xl text-neutral-900 antialiased sm:text-2xl">
    <section class="border-b border-neutral-300 bg-stone-100">
      <div class="mx-auto max-w-7xl px-4 py-5 sm:px-6 lg:px-8">
        <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
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

        <div class="mt-4 border-b border-neutral-300 pb-6">
          <div>
            <h1 class="max-w-4xl text-6xl font-normal leading-tight text-neutral-950 sm:text-7xl lg:text-9xl">
              Suikerterrein
            </h1>
            <p class="mt-4 max-w-3xl text-2xl leading-9 text-neutral-700 sm:text-3xl">
              {{ currentHeroImage.caption }}
            </p>
          </div>

          <div class="mt-8 overflow-x-auto">
            <div class="flex w-max gap-3 pb-3">
              <button
                v-for="(image, index) in heroImages"
                :key="image.src"
                type="button"
                class="group shrink-0 border bg-stone-50 p-1 transition duration-200"
                :class="currentHeroIndex === index ? 'border-neutral-950' : 'border-neutral-300 opacity-60 hover:border-neutral-600 hover:opacity-100'"
                :aria-label="`Show ${image.alt}`"
                @click="selectHeroImage(index)"
              >
                <img
                  :src="image.src"
                  :alt="image.alt"
                  class="h-20 w-28 object-cover grayscale transition duration-200 group-hover:grayscale-0 sm:w-32"
                  :class="currentHeroIndex === index ? 'grayscale-0' : ''"
                >
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <nav class="sticky top-0 z-20 border-b border-neutral-300 bg-stone-50/95 backdrop-blur">
      <div class="mx-auto max-w-7xl overflow-x-auto px-4 sm:px-6 lg:px-8">
        <div class="flex min-w-max items-center gap-8 py-5 text-lg uppercase tracking-[0.14em] text-neutral-600">
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
          <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
            Introduction
          </p>
          <h2 class="mt-4 text-5xl font-normal leading-tight text-neutral-950 sm:text-6xl">
            Artist Research: Suikerterrein
          </h2>
        </div>

        <div class="max-w-4xl text-2xl leading-10 text-neutral-700">
          <p>
            This website presents an artist research project about Suikerterrein, an artist and cultural community in Groningen that is expected to disappear around 2030 due to future redevelopment. Through interviews, we investigated how artists experience this place, how they build community, and what may be lost when such temporary cultural spaces are removed.
          </p>
        </div>
      </div>
    </section>

    <section class="border-b border-neutral-300 bg-[#ede8df]">
      <div class="mx-auto grid max-w-7xl gap-12 px-4 py-20 sm:px-6 md:grid-cols-[0.8fr_1.2fr] lg:px-8 lg:py-28">
        <div>
          <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
            Research ground
          </p>
          <h2 class="mt-4 text-5xl font-normal leading-tight text-neutral-950 sm:text-6xl">
            Motivation
          </h2>
        </div>

        <div class="max-w-4xl text-2xl leading-10 text-neutral-700">
          <p>
            Our motivation comes from a concern for temporary artist communities and the fragile spaces that support them. Suikerterrein is not only a physical location, but also a living network of artists, makers, events, memories, and informal support. By interviewing people connected to the site, we want to understand what this place means before it changes or disappears.
          </p>
        </div>
      </div>
    </section>

    <section id="about" class="scroll-mt-24 border-b border-neutral-300">
      <div class="mx-auto grid max-w-7xl gap-12 px-4 py-20 sm:px-6 md:grid-cols-[0.8fr_1.2fr] lg:px-8 lg:py-28">
        <div>
          <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
            Site notes
          </p>
          <h2 class="mt-4 text-5xl font-normal leading-tight text-neutral-950 sm:text-6xl">
            About Suikerterrein
          </h2>
          <p class="mt-5 max-w-md text-xl leading-8 text-neutral-600">
            A compact archive of context, temporary use, future redevelopment, and the cultural questions around the site.
          </p>
        </div>

        <div class="grid max-w-4xl gap-9">
          <article
            v-for="section in aboutSections"
            :key="section.title"
            class="border-t border-neutral-300 pt-6"
          >
            <h3 class="text-3xl font-normal leading-tight text-neutral-950 sm:text-4xl">
              {{ section.title }}
            </h3>
            <p class="mt-4 text-2xl leading-10 text-neutral-700">
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
            <p class="text-base uppercase tracking-[0.22em] text-stone-400">
              Oral archive
            </p>
            <h2 class="mt-4 text-5xl font-normal leading-tight sm:text-6xl">
              Interviews
            </h2>
          </div>

          <p class="max-w-4xl text-2xl leading-10 text-stone-300">
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
              <p class="text-base uppercase tracking-[0.18em] text-stone-400">
                Interview
              </p>
              <h3 class="mt-3 text-4xl font-normal text-stone-50">
                {{ interview.name }}
              </h3>
              <p class="mt-3 text-xl leading-8 text-stone-300">
                {{ interview.description }}
              </p>
              <p class="mt-5 text-xl leading-9 text-stone-200">
                {{ interview.summary }}
              </p>
              <blockquote class="mt-6 border-l border-stone-400 pl-4 text-xl italic leading-9 text-stone-200">
                "{{ interview.quote }}"
              </blockquote>
              <audio class="mt-6 w-full" controls :src="interview.audio" />
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="team" class="scroll-mt-24 bg-stone-50 px-4 py-20 sm:px-6 lg:px-8 lg:py-28">
      <div class="mx-auto max-w-7xl">
        <div class="mb-12 max-w-3xl">
          <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
            Team
          </p>
          <h2 class="mt-4 text-5xl font-normal leading-tight text-neutral-950 sm:text-6xl">
            Researchers
          </h2>
          <p class="mt-6 text-xl leading-8 text-neutral-600">
            This research was developed by four members through interviews, field observation, and artistic reflection.
          </p>
        </div>

        <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-4">
          <article
            v-for="member in teamMembers"
            :key="member.name"
            class="border border-neutral-300 bg-stone-100"
          >
            <img
              :src="member.image"
              :alt="member.name"
              class="aspect-[4/5] w-full object-cover grayscale-[15%]"
            >

            <div class="p-6">
              <p class="text-xs uppercase tracking-[0.24em] text-neutral-500">
                {{ member.role }}
              </p>

              <h3 class="mt-3 text-2xl font-medium text-neutral-900">
                {{ member.name }}
              </h3>

              <p class="mt-5 text-base leading-7 text-neutral-700">
                {{ member.bio }}
              </p>

              <div class="mt-6 border-t border-neutral-300 pt-5">
                <p class="text-xs uppercase tracking-[0.2em] text-neutral-500">
                  Reflection
                </p>
                <p class="mt-3 text-base leading-7 text-neutral-700">
                  {{ member.reflection }}
                </p>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>
  </main>
</template>
