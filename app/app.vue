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
  },
  {
    src: '/images/hero-9.jpeg',
    alt: 'Suikerterrein image 9',
    caption: 'Built fragments and shared working spaces'
  },
  {
    src: '/images/hero-10.jpeg',
    alt: 'Suikerterrein image 10',
    caption: 'Everyday materials inside the terrain'
  },
  {
    src: '/images/hero-11.jpeg',
    alt: 'Suikerterrein image 11',
    caption: 'Studios, workshops, and temporary structures'
  },
  {
    src: '/images/hero-12.jpeg',
    alt: 'Suikerterrein image 12',
    caption: 'Post-industrial space in active use'
  },
  {
    src: '/images/hero-13.jpeg',
    alt: 'Suikerterrein image 13',
    caption: 'Artist spaces shaped by time and reuse'
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
    name: 'Roeksrariteiten',
    label: 'Maruschka & Laurens / wonder / nature',
    image: '/images/interview-maruschka-laurens.jpeg',
    object: 'Nettle plant',
    audio: '/audio/maruschka-laurens.mp3',
    quote: 'Something that is rejected can actually be essential.',
    summary: 'Maruschka and Laurens work together through drawing, wonder, practical making, and a shared interest in reconnecting humans with nature.',
    profiles: [
      {
        name: 'Maruschka',
        text: 'Maruschka has been drawing all her life. During her time at art academy, it became clear to her that what you create can have an impact on people. It does not necessarily have to be art; it should evoke a sense of wonder. One of the most essential themes today, in her view, is reconnecting humans with nature.'
      },
      {
        name: 'Laurens',
        text: 'Laurens provides practical support. If he does not yet know how to do something, he learns it. From digital work to hands-on making and construction, he applies a wide range of skills to transform a good idea into a great one, especially when working with Maruschka\'s drawings.'
      }
    ],
    themes: ['Ecosystem', 'Weeds', 'Fairytale stories'],
    fragments: [
      {
        title: 'Community is more than proximity',
        text: 'They distinguish between people simply renting spaces next to each other and a community that actively works together. Suikerterrein contains artists and generous neighbors, but they see the social structure as fragmented, with commercial interests and individual territories shaping the terrain.'
      },
      {
        title: 'A practical condition for art',
        text: 'For them, the low rent was not romantic; it was what made it possible to build an artistic life after art school. Because less income disappears into rent, more energy and money can be invested back into their work.'
      },
      {
        title: 'Toward an ecological model',
        text: 'They imagine a smaller, more community-based and nature-focused future place: not a huge terrain of many companies, but a setting where ten to fifteen people could share a clearer philosophy.'
      }
    ]
  },
  {
    name: 'Robert',
    label: 'Stained glass / self-built studio',
    image: '/images/interview-robert.jpeg',
    object: 'A photograph of colored glass',
    audio: '/audio/robert.mp3',
    quote: 'We use the area with the uncertainty of life.',
    summary: 'Robert speaks about building his own studio from containers and second-hand materials, accepting the 2030 deadline, and seeing temporary creative places as necessary stepping stones in the city.',
    profiles: [],
    themes: ['Light', 'Colors', 'Uncertainty'],
    fragments: [
      {
        title: 'Building a place from what already lived',
        text: 'Robert designed and built his studio with containers, reused roof plates, old wood, found materials, and help from people with different skills. The building had to meet city rules, but its atmosphere came from making new use of materials with previous lives.'
      },
      {
        title: 'Certainty and openness',
        text: 'He knows 2030 may be the deadline, but does not want to worry too early. For him, uncertainty is part of how he lives and works: a few things must be stable, while the rest can stay open.'
      },
      {
        title: 'Stepping stones in the city',
        text: 'Robert connects Suikerterrein to earlier temporary cultural spaces in Groningen. These places let people meet, work, dance, learn, and briefly step outside ordinary city life; if one disappears, something else has to grow somewhere.'
      }
    ]
  },
  {
    name: 'Floris Maathuis',
    label: 'Creative explorations in technology',
    image: '/images/interview-floris.jpeg',
    object: 'Reused building materials',
    audio: '/audio/floris.mp3',
    quote: 'Almost everything here has a story.',
    summary: 'Floris Maathuis brings technology and creativity together into tailor-made solutions and innovations. Working with businesses, governments, social and cultural organizations, and many other clients, he develops creative technological approaches for social issues, communication, product innovation, and entertainment.',
    profiles: [],
    themes: ['Community', 'Creativity', 'Ecosystem'],
    fragments: [
      {
        title: 'From sugar factory to temporary initiatives',
        text: 'Floris explains the site through its industrial past: the former factory, the canal, the vloeivelden, and the decision to use the area for temporary initiatives after demolition.'
      },
      {
        title: 'A club of makers',
        text: 'The group organized itself like an association with members, shared contributions, crowdfunding, and borrowed money. Their spaces were assembled from second-hand structures: beach houses, garden sheds, army units, shipping containers, and other salvaged materials.'
      },
      {
        title: 'What survives after 2030',
        text: 'People are already talking with the city and lobbying for parts of what evolved here to be included in future development. The concern is not only preserving buildings, but preserving the possibility of making, gathering, and experimenting.'
      }
    ]
  }
]

const teamMembers = [
  {
    name: 'Yize Huang',
    role: 'Researcher / Artist',
    image: '/images/team-yize.jpg',
    bio: 'I am from Taipei, Taiwan. My practice often begins with the body, vulnerability, memory, and states of survival. I am interested in how people maintain their form under pressure, isolation, or unstable conditions, and how emotions that cannot be fully articulated leave traces through objects, text, and space. In my work, sculpture is not only an object, but also a body that continues to stand after being wounded. These sculptures may appear broken, tilted, or fragile, yet they remain placed within a space. Through damaged materials, repetition, and accumulation, I try to present a state of being unable to truly fall down: not because of strength, but because some people do not have the privilege to collapse.',
    reflection: 'This field research focuses on Suikerterrein, a former industrial site that has gradually become a place where art, events, and urban life intersect. Its transformation reminds me of similar spaces in Taiwan, such as old factories, warehouses, abandoned buildings, and marginal areas that have been reused by artists and communities. I am interested in how artistic ecosystems emerge in these places: why artists gather there, how they use or change the space, and how the space influences them. Through Suikerterrein, I hope to observe the relationship between artists, the city, and the changing life of a place.'
  },
  {
    name: 'YuTzu Hsu',
    role: 'Interdisciplinary Artist / Researcher',
    image: '/images/team-yuzu.png',
    bio: 'She is an interdisciplinary artist whose work often begins with observations of human culture, everyday life, and rituals. Through performance, collective making, and interventions, she explores how relationships between people are formed within specific situations.',
    reflection: 'Her practice often takes the form of artistic interventions and collective creation, focusing on experiences in everyday life that are difficult to articulate. She explores how bodily memory shapes personal histories and habitual rituals, and how interactions between people influence one another and contribute to the formation of cultural environments. Working with groups and the body as a medium, she tries to transform personal memory into situations that can be experienced and participated in by others, allowing relationships between individuals and collectives to emerge and shift.'
  },
  {
    name: 'Ayeen Fazel',
    role: 'Artist-facilitator / Researcher',
    image: '/images/team-Ayeen.jpeg',
    bio: 'Ayeen Fazel is an artist-facilitator based in Groningen, working at the intersection of installation, storytelling, and participatory practice. Her work focuses on creating spaces where people can explore questions of belonging, land, and human connection through shared experiences. Drawing from personal and collective research, she works with translucent materials, shadow, and text to construct environments where viewers become part of the work. Her practice is rooted in facilitation, inviting reflection through simple yet fundamental questions rather than fixed answers.',
    reflection: 'I’m very interested in this area because I find it amazing and different from other places in the city. I was curious about what is happening here, the history behind it, how this place became what it is today, and who the people are. I already had some information, but after talking with the artists, I gained a much clearer vision, along with different perspectives. What I found especially interesting is how they built something temporary, but at the same time created something that goes beyond that: an approach and way of living that can continue even after this place is gone.'
  },
  {
    name: 'Leila Mokhtari',
    role: 'Visual Artist / Ceramic Artist / Researcher',
    image: '/images/team-leila.png',
    bio: 'I was born in 1994 in Iran, and for almost ten years my main practice has been in the field of visual art and functional ceramics. My academic background is in sculpture, and most of the artworks I create are three-dimensional. Space is the most fundamental element of my projects, and it can fully represent my thoughts.',
    reflection: 'As I began working, I became interested in the concept of history and the passing of time, and I try to distinguish its connection with our contemporary world. I am also inspired by ancient architecture, literature, and their bonds with the human soul. While my main career is related to fine art, I launched a ceramic studio a couple of years ago, and a major part of my practice has focused on developing a pottery studio, learning how to collaborate, and making progress through shared work.'
  },
  {
    name: 'Shiva',
    role: 'Painter / Researcher',
    image: '/images/team-shiva.jpeg',
    bio: 'In my recent painting project, I use references to Iranian architectural geometry, tilework, and mirror structures to study adaptive visual sequences through return, shift, absence, fracture, and reconfiguration. Through this, I visually explore how coexistence can be imagined as a balance between autonomy and a shared condition: each work remains independent while responding to one recurring structural logic that connects the series without making it uniform.',
    reflection: 'I joined this project to extend this question into the context of the Suikerterrein, a temporary artistic community in a former industrial site. I am interested in how artists create continuity within a place whose current cultural use is being reshaped by planned redevelopment, shaped by presence, adaptation, and a shared environment. In conversations with the participating artists, I explore how this community contributes to the cultural memory of the site, leaving traces of presence, practice, and belonging that are not always officially preserved or visibly acknowledged.'
  }
]

const currentHeroIndex = ref(0)
const activeProfileIndexes = ref<Record<string, number>>({})
let heroInterval: ReturnType<typeof setInterval> | undefined

const currentHeroImage = computed(() => heroImages[currentHeroIndex.value])

const selectHeroImage = (index: number) => {
  currentHeroIndex.value = index
}

const getActiveProfileIndex = (name: string) => activeProfileIndexes.value[name] ?? 0

const selectProfile = (name: string, index: number) => {
  activeProfileIndexes.value = {
    ...activeProfileIndexes.value,
    [name]: index
  }
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
              class="aspect-[16/10] w-full object-cover grayscale-[20%] sm:aspect-auto sm:h-[68vh] sm:min-h-[360px]"
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

    <section id="interviews" class="scroll-mt-24 border-b border-neutral-300 bg-[#23312d] text-stone-50">
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
            Three conversations trace Suikerterrein through self-built studios, informal support, ecological thinking, temporary land use, and the question of what may remain after 2030.
          </p>
        </div>

        <div class="mt-14 grid gap-10 lg:grid-cols-[0.34fr_0.66fr]">
          <aside class="border-t border-stone-500 pt-6 lg:sticky lg:top-28 lg:self-start">
            <p class="text-base uppercase tracking-[0.22em] text-stone-400">
              Interviewees
            </p>
            <div class="mt-6 grid gap-5">
              <a
                v-for="interview in interviews"
                :key="interview.name"
                :href="`#interview-${interview.name.toLowerCase().replaceAll(' ', '-').replaceAll('&', 'and')}`"
                class="group border-l border-stone-500 pl-5 transition duration-200 hover:border-stone-100"
              >
                <span class="block text-2xl leading-tight text-stone-100">
                  {{ interview.name }}
                </span>
                <span class="mt-2 block text-base leading-6 text-stone-400 group-hover:text-stone-300">
                  {{ interview.label }}
                </span>
              </a>
            </div>
          </aside>

          <div class="grid gap-8">
            <article
              v-for="interview in interviews"
              :id="`interview-${interview.name.toLowerCase().replaceAll(' ', '-').replaceAll('&', 'and')}`"
              :key="interview.name"
              class="scroll-mt-32 border border-stone-600 bg-[#1f2a27]"
            >
              <div class="grid">
                <img
                  :src="interview.image"
                  :alt="`${interview.name} interview material`"
                  class="aspect-[16/9] w-full object-cover grayscale-[20%]"
                >

                <div class="grid gap-8 p-6 sm:p-8 lg:grid-cols-[0.38fr_0.62fr]">
                  <div>
                    <p class="text-base uppercase tracking-[0.18em] text-stone-400">
                      {{ interview.label }}
                    </p>
                    <h3 class="mt-3 text-4xl font-normal leading-tight text-stone-50 sm:text-5xl">
                      {{ interview.name }}
                    </h3>

                    <blockquote class="mt-7 border-l border-stone-300 pl-5 text-2xl italic leading-9 text-stone-100">
                      "{{ interview.quote }}"
                    </blockquote>
                  </div>

                  <div>
                    <p class="text-lg leading-8 text-stone-200 sm:text-xl">
                      {{ interview.summary }}
                    </p>

                    <div
                      v-if="interview.profiles.length"
                      class="mt-7 border-t border-stone-600 pt-5"
                    >
                      <div class="grid grid-cols-2 gap-2">
                        <button
                          v-for="(profile, profileIndex) in interview.profiles"
                          :key="profile.name"
                          type="button"
                          class="min-h-12 border px-4 py-3 text-left text-base leading-6 transition duration-200"
                          :class="getActiveProfileIndex(interview.name) === profileIndex ? 'border-stone-100 bg-stone-100 text-[#1f2a27]' : 'border-stone-600 text-stone-300 hover:border-stone-300 hover:text-stone-100'"
                          @click="selectProfile(interview.name, profileIndex)"
                        >
                          {{ profile.name }}
                        </button>
                      </div>

                      <div class="mt-5 min-h-[14rem] border-l border-stone-500 pl-5">
                        <p class="text-lg leading-8 text-stone-100">
                          {{ interview.profiles[getActiveProfileIndex(interview.name)].text }}
                        </p>
                      </div>
                    </div>

                    <div class="mt-7 grid gap-4 border-t border-stone-600 pt-6 sm:grid-cols-2">
                      <div>
                        <p class="text-sm uppercase tracking-[0.18em] text-stone-400">
                          Offered object
                        </p>
                        <p class="mt-2 text-xl leading-7 text-stone-100">
                          {{ interview.object }}
                        </p>
                      </div>

                      <div>
                        <p class="text-sm uppercase tracking-[0.18em] text-stone-400">
                          Key themes
                        </p>
                        <div class="mt-3 flex flex-wrap gap-2">
                          <span
                            v-for="theme in interview.themes"
                            :key="theme"
                            class="border border-stone-500 px-3 py-1 text-base leading-6 text-stone-200"
                          >
                            {{ theme }}
                          </span>
                        </div>
                      </div>
                    </div>

                    <div class="mt-7 border-t border-stone-600 pt-6">
                      <p class="text-sm uppercase tracking-[0.18em] text-stone-400">
                        Recording
                      </p>
                      <audio class="mt-4 w-full" controls preload="none" :src="interview.audio" />
                    </div>
                  </div>
                </div>
              </div>

              <div class="border-t border-stone-600">
                <details
                  v-for="fragment in interview.fragments"
                  :key="fragment.title"
                  class="group border-b border-stone-700 last:border-b-0"
                >
                  <summary class="flex cursor-pointer list-none items-center justify-between gap-4 px-6 py-5 text-xl leading-7 text-stone-100 transition duration-200 hover:bg-stone-100/5 sm:px-8">
                    <span>{{ fragment.title }}</span>
                    <span class="text-2xl leading-none text-stone-400 transition duration-200 group-open:rotate-45">+</span>
                  </summary>
                  <p class="px-6 pb-7 text-xl leading-9 text-stone-300 sm:px-8">
                    {{ fragment.text }}
                  </p>
                </details>
              </div>
            </article>
          </div>
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
            This research was developed by five members through interviews, field observation, and artistic reflection.
          </p>
        </div>

        <div class="grid gap-6">
          <article
            v-for="member in teamMembers"
            :key="member.name"
            class="grid overflow-hidden border border-neutral-300 bg-stone-100 lg:grid-cols-[18rem_1fr]"
          >
            <img
              :src="member.image"
              :alt="member.name"
              class="aspect-[4/5] w-full object-cover grayscale-[15%] lg:h-full"
            >

            <div class="p-6 sm:p-8">
              <p class="text-xs uppercase tracking-[0.24em] text-neutral-500">
                {{ member.role }}
              </p>

              <h3 class="mt-3 text-3xl font-medium text-neutral-900">
                {{ member.name }}
              </h3>

              <div class="mt-6 grid gap-6 xl:grid-cols-2">
                <div>
                  <p class="text-xs uppercase tracking-[0.2em] text-neutral-500">
                    Practice
                  </p>
                  <p class="mt-3 text-base leading-8 text-neutral-700">
                    {{ member.bio }}
                  </p>
                </div>

                <div class="border-t border-neutral-300 pt-5 xl:border-l xl:border-t-0 xl:pl-6 xl:pt-0">
                  <p class="text-xs uppercase tracking-[0.2em] text-neutral-500">
                    Project focus
                  </p>
                  <p class="mt-3 text-base leading-8 text-neutral-700">
                    {{ member.reflection }}
                  </p>
                </div>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>
  </main>
</template>
