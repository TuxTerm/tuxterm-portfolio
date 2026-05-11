<script>
  const calculateAge = (dob) => {
    const diffMs = Date.now() - new Date(dob).getTime();
    const ageDt = new Date(diffMs); 
    return Math.abs(ageDt.getUTCFullYear() - 1970);
  };
  const age = calculateAge('2001-12-04');
</script>

<section id="about">
  <h1><span class="highlight">sudo whoami</span></h1>
  <p>
    Hey there! I'm <strong>Rishu Raj</strong>. I'm a {age}-year-old carbon-based lifeform operating out of Haryana, India. I spend most of my time trying to make computers do things they weren't strictly designed to do (legally, of course) and figuring out how to stop others from doing the same. 
  </p>

  <h3>The Tech Side</h3>
  <p>
    My brain runs on a highly customized logic engine. When I'm not studying Information Security, I'm deep into ethical hacking, reverse engineering, and trying to figure out why the network went down (spoiler: it's always DNS). I break things on purpose so bad guys can't break them by accident.
  </p>

  <h3>My System</h3>
  <p>
    I daily drive Linux because I enjoy having absolute control and the occasional thrill of fixing a broken bootloader. You can inspect my current loadout, applications, and terminal setup over at <a href="#/tools">Tools</a>.
  </p>
  
  <br/>
  <h3>Certifications</h3>
  <ul>
    <li>Harvard's CS50, CS50P-Python</li>
  </ul>

  <h3>Achievements</h3>
  <ul>
    <li>Secured AIR 41st on NCIIPC-AICTE Pentathon 2025 FINALE.</li>
    <li>Attended NCIIPC-AICTE Pentathon 2026 Bootcamp at MIT Manipal and interacted with various industry leaders. </li>
  </ul>
</section>

<style>
  .highlight {
    background-color: var(--accent);
    color: var(--bg);
    padding: 0.2rem 0.5rem;
    display: inline-block;
  }
</style>
