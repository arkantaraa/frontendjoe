<template>
  <div class="wrapper">
    <div class="about-subtitle">
      Skills
    </div>
    <div class="skills-subtitle">
      Development
    </div>
    <div class="skills-list">
      <div class="skills-list-item" v-for="skill in devSkills" :key="skill">
        {{ skill }}
      </div>
    </div>
    <div class="skills-subtitle">
      Design
    </div>
    <div class="skills-list">
      <div class="skills-list-item" v-for="skill in designSkills" :key="skill">
        {{ skill }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      devSkills: [
        "React",
        "Vue",
        "Angular",
        "Node",
        "HTML",
        "CSS",
        "SCSS",
        "Git",
        "Styled Components",
        "React Native"
      ],
      designSkills: ["Sketch", "Figma", "Adobe XD", "Illustrator", "Photoshop"]
    };
  }
};
</script>

<style lang="scss" scoped>
@import "assets/scss/variables.scss";

.wrapper {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  padding: 2rem 0;

  @media (min-width: $screenWidthMd) {
    padding: 0;
  }
}

.skills-subtitle {
  font-size: 0.875rem;
  font-weight: 800;
  color: $colorPrimary;
  margin-bottom: 0.75rem;
}

.skills-list {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-wrap: wrap;
  width: 100%;
  margin-bottom: 2rem;

  @media (min-width: $screenWidthMd) {
    width: 258px;
    max-width: 258px;
  }
}

.skills-list-item {
  height: 50px;
  font-size: 0.875rem;
  font-weight: 600;
  color: rgba(0, 0, 0, 0.5);
  padding: 0 0.25rem;
  display: flex;
  align-items: center;
  border-bottom: 1px solid rgba(0, 0, 0, 0.125);
  margin-right: 0.5rem;
}
</style>
