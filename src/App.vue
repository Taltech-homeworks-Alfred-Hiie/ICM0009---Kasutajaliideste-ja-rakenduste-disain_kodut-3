<template>
  <div class="phases-display">
    <PhaseComponent
      :phaseTitle="'Etapp 1'"
      :actions="['Vastab kõnele', 'Üritab kliendi murest aru saada']"
      :phaseText="'Sellise murega pole ma küll enne tegelenud... Kuidas see üldse juhtus? 🙁'"
      :phaseColor="'#a7c2ed'"
    />
    <PhaseComponent
      :phaseTitle="'Etapp 2'"
      :actions="[
        'Sirvib hooldusäppi',
        'Avab järjest erinevaid projekte, kus võiks midagi sarnast olla',
        'Vaatab läbi Jiras tehtud tööd',
      ]"
      :phaseText="'Tundub, et tõesti ei ole sellega enne kokku puutunud. 😐'"
      :phaseColor="'#8a89db'"
    />
    <PhaseComponent
      :phaseTitle="'Etapp 3'"
      :actions="[
        'Otsib Jirast',
        'Otsib Microsoft Plannerist, mida Soome osakond kasutab',
        'Lõpetab kõne ja lubab meili teel vastata',
      ]"
      :phaseText="'Ei suuda leida, et keegi teinegi sellega oleks tegelnud. 🙁'"
      :phaseColor="'#c081e6'"
    />
    <PhaseComponent
      :phaseTitle="'Etapp 4'"
      :actions="[
        'Küsib kolleegidelt',
        'Oma osakonna töötajad ei tea',
        'Automaatika osakonnast vastatakse, et dokumentides on kirjas.',
      ]"
      :phaseText="'Väga hea, kohe otsin dokumendi. 😊'"
      :phaseColor="'#ef8cc7'"
    />
    <PhaseComponent
      :phaseTitle="'Etapp 5'"
      :actions="[
        'Sirvib läbi kolm dokumenti',
        'Neljas dokument on 46 lehekülge',
        'Find funktsioon kah ei leia',
      ]"
      :phaseText="'Otsib kuni pea kärssab. Ei ole ju kusagil. 😠 '"
      :phaseColor="'#f9a779'"
    />
    <PhaseComponent
      :phaseTitle="'Etapp 6'"
      :actions="[
        'Läheb automaatika osakonda kohale',
        'Pikka otsimise peale leitaksegi õige asi üles',
        'Võtab vajaliku info ja läheb kirjutab kliendile meili vastu',
      ]"
      :phaseText="'Kas see tõesti kuidagi kergemini ei saaks toimida? 😟'"
      :phaseColor="'#e96b6b'"
    />
  </div>
</template>

<script>
import PhaseComponent from "./components/PhaseComponent.vue";

export default {
  components: {
    PhaseComponent,
  },
};
</script>

<style scoped>
.phases-display {
  display: flex;
  justify-content: center;
  flex-wrap: nowrap; /* Prevents wrapping to the next line */
  padding: 20px;
}
</style>
