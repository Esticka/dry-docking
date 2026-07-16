<template>
  <div class="layout">

    <Sidebar />

    <div class="content">

      <Header />

      <div class="page">

        <!-- Quotes Pending Approval -->
        <section class="section">
          <h2>Quotes Pending Approval</h2>

          <div class="board">
            <ShipColumn
              v-for="ship in ships"
              :key="ship.id"
              :ship="ship"
            />
          </div>
        </section>

        <!-- Pending Yard Quotes -->
        <section class="section">
          <h2>Pending Yard Quotes</h2>

          <div class="board">
            <PendingYardColumn
              v-for="ship in ships"
              :key="'yard-' + ship.id"
              :ship="ship"
            />
          </div>
        </section>

        <!-- Jobs Awaiting Dock -->
        <section class="section">
          <h2>Jobs Awaiting Dock</h2>

          <div class="board">
            <JobColumn
              v-for="dock in dockJobs"
              :key="dock.title"
              :title="dock.title"
              :jobs="dock.jobs"
            />
          </div>
        </section>

        <!-- Active Dry Docks -->
        <section class="section">

          <h2>Active Dry Docks</h2>

          <div class="summary">

            <div class="summary-card">
              <h1>12</h1>
              <p>Open</p>
            </div>

            <div class="summary-card">
              <h1>5</h1>
              <p>In Progress</p>
            </div>

            <div class="summary-card">
              <h1>18</h1>
              <p>Completed</p>
            </div>

            <div class="summary-card">
              <h1>2</h1>
              <p>On Hold</p>
            </div>

          </div>

        </section>

        <!-- Costs -->
        <section class="section">

          <h2>Costs</h2>

          <table class="cost-table">

            <thead>
              <tr>
                <th>Ship</th>
                <th>Budget</th>
                <th>Actual</th>
              </tr>
            </thead>

            <tbody>

              <tr>
                <td>Ocean Star</td>
                <td>$120,000</td>
                <td>$110,000</td>
              </tr>

              <tr>
                <td>MV Glory</td>
                <td>$95,000</td>
                <td>$90,000</td>
              </tr>

              <tr>
                <td>MV Happy</td>
                <td>$150,000</td>
                <td>$132,000</td>
              </tr>

            </tbody>

          </table>

        </section>

      </div>

    </div>

  </div>
</template>

<script setup>

import Sidebar from '../components/sidebar.vue'
import Header from '../components/header.vue'
import ShipColumn from '../components/shipcolumn.vue'
import PendingYardColumn from '../components/pendingyardcolumn.vue'
import JobColumn from '../components/jobcolumn.vue'

const ships = [

  {
    id:1,
    name:'OCEAN STAR',
    company:'Kempell',
    code:'SEPT2020/DD1'
  },

  {
    id:2,
    name:'MV GLORY',
    company:'Bombay Dockyard',
    code:'SEPT2020/DD2'
  },

  {
    id:3,
    name:'MV HAPPY',
    company:'Hindustan Shipyard',
    code:'OCT2020/DD1'
  }

]

const dockJobs = [

  {
    title: 'Dock A',

    jobs: [

      {
        id: 1,
        title: 'Main Engine Inspection',
        code: 'ENG-101',
        type: 'Inspection'
      },

      {
        id: 2,
        title: 'Cooling Pump Service',
        code: 'ENG-205',
        type: 'Maintenance'
      },

      {
        id: 3,
        title: 'Generator Performance Test',
        code: 'GEN-301',
        type: 'Electrical'
      }

    ]

  },

  {
    title: 'Dock B',

    jobs: [

      {
        id: 4,
        title: 'Hull Surface Cleaning',
        code: 'HUL-110',
        type: 'Cleaning'
      },

      {
        id: 5,
        title: 'Anchor Chain Check',
        code: 'ANC-220',
        type: 'Inspection'
      },

      {
        id: 6,
        title: 'Propeller Alignment',
        code: 'PRP-115',
        type: 'Mechanical'
      }

    ]

  },

  {
    title: 'Dock C',

    jobs: [

      {
        id: 7,
        title: 'Fuel Tank Examination',
        code: 'FLT-510',
        type: 'Inspection'
      },

      {
        id: 8,
        title: 'Navigation System Test',
        code: 'NAV-410',
        type: 'Electrical'
      },

      {
        id: 9,
        title: 'Valve Replacement',
        code: 'VAL-710',
        type: 'Repair'
      },

      {
        id: 10,
        title: 'Emergency Pump Check',
        code: 'PMP-810',
        type: 'Maintenance'
      }

    ]

  }

]

</script>

<style scoped>

.layout{
  display:flex;
  min-height:100vh;
}

.content{
  flex:1;
}

.page{
  padding:30px;
  background:#f4f6f9;
  min-height:calc(100vh - 80px);
}

.section{
  margin-bottom:45px;
}

.section h2{
  margin-bottom:20px;
  color:#333;
}

.board{
  display:flex;
  gap:20px;
  overflow-x:auto;
}

.summary{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:20px;
}

.summary-card{
  background:white;
  border-radius:10px;
  padding:25px;
  text-align:center;
  border:1px solid #e5e5e5;
  box-shadow:0 2px 5px rgba(0,0,0,.05);
}

.summary-card h1{
  color:#2f90e8;
  font-size:32px;
  margin-bottom:10px;
}

.summary-card p{
  color:#666;
}

.cost-table{
  width:100%;
  background:white;
  border-collapse:collapse;
  border-radius:10px;
  overflow:hidden;
}

.cost-table th{
  background:#2f90e8;
  color:white;
  padding:15px;
  text-align:left;
}

.cost-table td{
  padding:15px;
  border-bottom:1px solid #ececec;
}

.cost-table tr:hover{
  background:#f7f9fc;
}

</style>