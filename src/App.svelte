<!-- Thomas McCoy -->

<script>
  import { Router, Link, Route } from "svelte-routing";
  import LiveFeed from "./routes/LiveFeed.svelte";
  import DoctorUpdates from "./routes/DoctorUpdates.svelte";
  import Appointments from "./routes/Appointments.svelte";
  import FeelingsTracker from "./routes/FeelingsTracker.svelte";
</script>


<body>
  <div class="page">
    <Router>
      <Route path="/">
        <h1>Thomas McCoy</h1>
        <Link id="liveFeed" to="/live-feed">
          <button class="options"> Live Feed</button>
        </Link>
        <Link id="appointments" to="/appointments">
          <button class="options"> Appointments</button>
        </Link>
        <Link id="doctorUpdates" to="/doctor-updates">
          <button class="options"> Doctor's Updates</button>
        </Link>
        <Link id="feelingsTracker" to="/feelings-tracker">
          <button class="options"> Feelings Tracker</button>
        </Link>
      </Route>
      <Route path="live-feed" component={LiveFeed} />
      <Route path="appointments" component={Appointments} />
      <Route path="doctor-updates" component={DoctorUpdates} />
      <Route path="feelings-tracker" component={FeelingsTracker} />
    </Router>
  </div>
</body>

<style>
  .page {
    height: 600px;
    width: 400px;
    align-items: center;
    border-radius: 25px;
    background-color: rgb(184, 229, 255);
    margin: auto;
  }

  .options {
    height: 125px;
    width: 350px;
    align-items: center;
    font-size: 25px;
    margin-top: 8px;
    margin-bottom: 2px;
  }

  h1 {
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }
</style>