#Explanation
<h2>AquaLife Coastal Watch – MERN Stack System Architecture</h2>

<h3> Frontend (React)</h3>
<ul>
  <li>User interface for citizens/volunteers.</li>
  <li>Capture geo-tagged images/videos of coastal issues.</li>
  <li>Add descriptions and categories (pollution, wildlife, waste).</li>
  <li>View reports and alerts dynamically.</li>
  <li>Sends REST API requests to backend.</li>
</ul>

<h3> Backend (Node.js + Express)</h3>
<ul>
  <li>Processes requests from frontend.</li>
  <li>User authentication using JWT (secure login).</li>
  <li>Report management: validate, store, and retrieve reports.</li>
  <li>Optional AI integration for waste/pollution detection.</li>
  <li>Acts as bridge between client and database.</li>
</ul>

<h3> Database (MongoDB)</h3>
<ul>
  <li>Stores all application data in collections.</li>
  <li><strong>Users</strong> → login info, roles, activity.</li>
  <li><strong>Reports</strong> → pollution sightings, wildlife observations, waste records.</li>
  <li><strong>Admin</strong> → approvals, monitoring logs.</li>
  <li>NoSQL structure allows flexibility and scalability.</li>
</ul>

<h3> Admin Dashboard</h3>
<ul>
  <li>Admins view and verify user reports.</li>
  <li>Approve or reject submissions.</li>
  <li>Monitor pollution trends with analytics.</li>
  <li>Communicates with backend via REST API.</li>
</ul>

<h3>Data Flow</h3>
<ol>
  <li>User (React) submits report → Backend (Express/Node).</li>
  <li>Backend validates and stores in MongoDB.</li>
  <li>Admin Dashboard retrieves data → verifies/approves.</li>
  <li>Approved reports → sent back to Frontend for public visibility.</li>
</ol>

<h3> Summary</h3>
<ul>
  <li><strong>React</strong> = user-facing interface.</li>
  <li><strong>Node + Express</strong> = server logic & APIs.</li>
  <li><strong>MongoDB</strong> = data storage.</li>
  <li><strong>Admin Dashboard</strong> = monitoring & decision-making.</li>
</ul>
