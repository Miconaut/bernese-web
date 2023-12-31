<script>
    export default {
        data() {
            const posts = ([
                {
                    title: 'O plemeni',
                    subtitle: 'Bernský salašnický pes v několika slovech.',
                    text1: 'Bernští salašníci pocházejí z Alp, kde byli původně využíváni jako ovčáci a tažná zvířata. Jsou to středně velcí psi s krásnou černobílou kresbou na srsti. Jejich klidná povaha a oddanost dělají z bernského salašnického psa vynikajícího společníka pro rodiny i jednotlivce. Toto plemeno je známé svou schopností rychle se přizpůsobit různým životním podmínkám.',
                    text2: 'Pokud máte rádi venkovský život, dlouhé procházky a společnost přátelského psa, bernský salašnický pes může být pro vás ideální volbou. Jejich inteligence a snadná cvičitelnost dělají z nich skvělého společníka pro rodiny s dětmi i bez.'
                },
                {
                    title: 'Průvodce výběrem',
                    subtitle: 'Je bernský salašnický pes pro vás?',
                    text1: 'Přemýšlíte o tom, jestli je bernský salašnický pes to pravé plemeno pro vás? Zde najdete informace o temperamentu, potřebách a zvláštnostech této plemenné krasavice. Bernští salašníci jsou známí svou klidnou povahou a vynikajícím vztahem k dětem. Jejich silný instinkt ochránce činí z nich skvělého strážce domova.',
                    text2: 'Předtím než si pořídíte bernského salašnického psa, je důležité zvážit jejich potřeby v pohybu a sociální interakci. Jsou to psi, kteří potřebují dostatek fyzické aktivity, a proto jsou ideální pro aktivní rodiny, které rády tráví čas venku. Přestože jsou to velcí psi, jejich přizpůsobivá povaha z nich dělá vynikající společníky i pro bytový život.'
                },
                {
                    title: 'Péče a výchova',
                    subtitle: 'Základy pro nové majitele.',
                    text1: 'Chcete vědět, jak správně pečovat o svého bernského salašnického psa? Získáte tipy ohledně stravování, cvičení a sociálního začleňování do rodiny. Bernští salašníci mají hustou srst, a proto je důležité věnovat pozornost pravidelnému kartáčování, aby byla udržována v optimálním stavu. Přestože jsou obecně zdraví psi, je důležité pravidelně navštěvovat veterináře a sledovat jejich hmotnost a celkový stav.',
                    text2: 'Výcvik bernského salašnického psa může být radostným zážitkem, protože jsou to chytrá a poslušná plemena. Kladná posílení a trpělivost jsou klíčové při výcviku. Pokud jste novým majitelem tohoto plemene, může být užitečné zapojit se do poslušnostních tříd, kde můžete získat rady od zkušených trenérů a zároveň posilnit pouto se svým psem.'
                },
                {
                    title: 'Zdraví a prevence',
                    subtitle: 'Jak ochránit vašeho čtyřnohého přítele.',
                    text1: 'Zde se dozvíte o typických zdravotních problémech spojených s bernským salašnickým psem a jak je prevencí minimalizovat. Zdraví vašeho psa má pro nás nejvyšší prioritu. Bernští salašníci jsou obecně zdravá plemena, ale jako každý pes jsou náchylní k určitým genetickým podmínkám. Pravidelná veterinární péče a kontrola jsou klíčové pro zachování jejich zdraví.',
                    text2: 'Vzhledem k jejich velikosti mohou bernští salašníci mít náchylnost k onemocněním kloubů, a proto je důležité sledovat jejich váhu a poskytovat jim kvalitní stravu. Pravidelné procházky a cvičení jsou také důležité pro udržení jejich fyzické kondice. Sledujte známky jakýchkoli potenciálních problémů a okamžitě konzultujte s veterinářem, pokud máte obavy o zdraví svého psa.'
                },
                {
                    title: 'Cvičení a hry',
                    subtitle: 'Aktivní život s bernským salašnickým psem.',
                    text1: 'Bernští salašníci jsou energičtí a milují pohyb. Zde naleznete tipy na cvičení a hry, které budou prospěšné jak vašemu psu, tak vám. Pravidelná fyzická aktivita je klíčová pro šťastný a vyvážený život bernského salašnického psa. Výlety na dlouhé procházky, hry na venkovním prostranství a sporty jako je agility jsou skvělým způsobem, jak udržovat jejich energii pod kontrolou a posílit váš vztah.',
                    text2: 'Pokud žijete v místě s dostatkem volného prostoru, neváhejte využít příležitosti k venkovnímu cvičení. Bernští salašníci jsou také skvělí společníci pro různé druhy sportů a poslušnostního cvičení. Můžete je zapojit do aktivit, které stimulují jejich mysli i těla, jako jsou hledání předmětů nebo interaktivní hračky.'
                },
                {
                    title: 'Společenství bernských salašnických psů',
                    subtitle: 'Setkávání a akce.',
                    text1: 'Připojte se k místním setkáním majitelů Bernských salašnických psů a zapojte se do společenství. Sdílejte zkušenosti a vytvářejte nová přátelství. Společenství majitelů bernských salašnických psů může být neocenitelné pro vás i vašeho psa. Setkávání s ostatními majiteli plemen podobné velikosti a povahy může být nejen zábavné, ale také užitečné pro výměnu rad a tipů.',
                    text2: 'Mnoho místních skupin pořádá akce a výlety pro majitele bernských salašnických psů. To může být skvělá příležitost pro vašeho psa socializovat se s jinými psy a pro vás poznat nové přátele. Sdílení svých zkušeností a rad v rámci komunity může také pomoci v překonávání různých výzev spojených s péčí o toto plemeno.'
                },
                {
                    title: 'Fotogalerie',
                    subtitle: 'Krása a půvab bernských salašnických psů.',
                    text1: 'Podívejte se na naši fotogalerii plnou úžasných snímků bernských salašnických psů poslaných naší komunitou. Každý pes je jedinečný a krásný! Naše galerie je místo, kde můžete sdílet fotografie svého bernského salašnického psa a prohlížet si úžasné obrázky od ostatních majitelů.',
                    text2: 'Můžete se nechat inspirovat různými pózami, prostředími a situacemi, které zdůrazňují krásu a jedinečnost tohoto plemene. Přidávání fotografií svého psa může být také zábavným způsobem, jak se podělit o svou radost z každodenního života s bernským salašnickým psem.'
                }
            ])

            return {
                posts
            }
        }
    }
</script>

<template>
    <div class="intro">
        <h1>Vítejte na stránce o bernském salašnickém psu!</h1>
        <p>Vítejte v komunitě milovníků bernských salašnických psů! Jestliže jste novým majitelem tohoto úžasného plemene, jste na správném místě. Bernští salašníci jsou známí svou přátelskou povahou, krásným vzhledem a věrností svým rodinám. Na této stránce najdete užitečné informace a rady pro optimální péči a šťastný život s vaším novým členem rodiny.</p>
        <p>Naše komunita sdružuje nadšené majitele bernských salašnických psů z celého světa. Připojte se k nám a podělte se o své zážitky, otázky a radosti spojené s tímto úžasným plemenem. Jsme tu, abychom vám pomohli v každém kroku na cestě vaším novým dobrodružstvím s bernským salašnickým psem!</p>
    </div>

    <div class="article" v-for="(item, key) in posts" :key="key">
        <div class="title">
            <h2>{{ item.title }}</h2>
            <h3>{{ item.subtitle }}</h3>
        </div>
        <div class="text">
            <p>{{ item.text1 }}</p>
            <p>{{ item.text2 }}</p>
        </div>
    </div>
</template>

<style scoped>
    h1, h2, h3 {
        font-family: 'Bebas Neue', sans-serif;
        font-weight: bold;

        letter-spacing: 0.05rem;
    }
    h1, h2 {
        color: #FDC921;
    }
    h1 {
        margin-bottom: 2.5rem;

        font-size: 2.5rem;
        text-align: center;
    }
    h2 {
        font-size: 2rem;
    }
    h3 {
        font-size: 1.5rem;
        color: #6798C0;
    }
    
    .intro, .article, .text {
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
    }

    .intro, .article {
        margin-bottom: 2rem;
    }
</style>