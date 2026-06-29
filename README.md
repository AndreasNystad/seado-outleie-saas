# seado-outleie-saas
{"name": "seadoo-saas",
  "version": "1.0.0",
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start"
  },
  "dependencies": {
    "next": "latest",
    "react": "latest",
    "react-dom": "latest",
    "@supabase/supabase-js": "latest",
    "@fullcalendar/react": "latest",
    "@fullcalendar/daygrid": "latest"
  }
}export default function Home() {
  return (
    <div style={{ padding: 40, fontFamily: "Arial" }}>
      
      <h1>🌊 Sea-Doo Spark Trixx Utleie</h1>
      <p>Book vannscooter på sekunder</p>

      <a href="/booking">
        <button style={{
          padding: 12,
          background: "black",
          color: "white",
          borderRadius: 10,
          marginTop: 20
        }}>
          Book nå
        </button>
      </a>

    </div>
  );
}"use client";

import { useState } from "react";

export default function Booking() {
  const [type, setType] = useState("dag");

  return (
    <div style={{ padding: 40 }}>
      
      <h1>📅 Booking</h1>

      <select onChange={(e) => setType(e.target.value)}>
        <option value="dag">Dagsleie</option>
        <option value="uke">Ukesleie (man–fre)</option>
      </select>

      <br /><br />

      <button style={{
        padding: 12,
        background: "blue",
        color: "white",
        borderRadius: 10
      }}>
        Betal med Vipps (demo)
      </button>

    </div>
  );
}import { createClient } from "@supabase/supabase-js";

export const supabase = createClient(
  process.env.NEXT_PUBLIC_SUPABASE_URL!,
  process.env.NEXT_PUBLIC_SUPABASE_ANON_KEY!
);module.exports = {
  reactStrictMode: true
};NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
VIPPS_TOKEN=
