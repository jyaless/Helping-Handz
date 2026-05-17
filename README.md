459-              { id: 'map', icon: MapIcon, label: 'Map' },
460-              { id: 'system', icon: Activity, label: 'Status' }
461:            ].map((item) => (
462-              <button
463-                key={item.id}
--
661-                            { id: 'private', label: 'Private' },
662-                            { id: 'none', label: 'None' }
663:                          ].map((i) => (
664-                            <button
665-                              key={i.id}
--
676-                        <label className="text-[10px] font-black text-slate-400 uppercase mb-3 block tracking-widest">Identify Gender</label>
677-                        <div className="grid grid-cols-3 gap-3">
678:                          {['male', 'female', 'lgbtq+'].map((g) => (
679-                            <button
680-                              key={g}
--
698-                            { id: 'domestic_violence', label: 'Domestic Violence' },
699-                            { id: 'child_care_pregnancy', label: 'Child Care & Pregnancy' }
700:                          ].map((c) => (
701-                            <button
702-                              key={c.id}
--
718-                            { id: 'stabilized', label: 'Stabilized' },
719-                            { id: 'crisis', label: 'Mental Crisis' }
720:                          ].map((s) => (
721-                            <button
722-                              key={s.id}
--
812-                                { item: "Phone Charger", priority: "Helpful" },
813-                                { item: "Clean Socks (2 pair)", priority: "Essential" }
814:                              ].map((check, idx) => (
815-                                <button 
816-                                  key={idx} 
--
897-                        Write My Own
898-                      </button>
899:                      {exampleNotes.map((note, i) => (
900-                        <button 
901-                          key={i}
--
987-                                      const findText = (node: any): string => {
988-                                        if (typeof node === 'string') return node;
989:                                        if (Array.isArray(node)) return node.map(findText).join(' ');
990-                                        if (node?.props?.children) return findText(node.props.children);
991-                                        return '';
--
1062-                              <div className="space-y-3">
1063-                                {status.references
1064:                                  .map(ref => {
1065-                                    // Try to find geocoded coords for this reference
1066-                                    const geo = geocodedRefs.find(g => g.title === ref.name);
--
1084-                                  .filter(ref => ref.dist !== null)
1085-                                  .sort((a, b) => (a.dist || 0) - (b.dist || 0))
1086:                                  .map((ref, idx) => (
1087-                                    <div key={idx} className="flex items-center justify-between p-4 bg-slate-50/50 rounded-2xl border border-slate-100 group hover:border-blue-200 transition-colors">
1088-                                      <div className="flex-1 min-w-0">
--
1141-                              </div>
1142-                              <div className="grid grid-cols-1 md:grid-cols-2 gap-3">
1143:                                {status.references.map((ref, idx) => (
1144-                                  <div key={idx} className="p-4 bg-white/60 backdrop-blur-sm rounded-xl border border-white group hover:border-pink-300 transition-all shadow-sm">
1145-                                    <div className="flex justify-between items-start mb-2">
--
1191-                                 </p>
1192-                                 <div className="grid grid-cols-1 gap-2">
1193:                                   {status.backup_options.map((backup, i) => (
1194-                                     <div key={i} className="bg-white/80 p-3 rounded-xl border border-white shadow-sm flex items-center justify-between gap-4 group hover:ring-2 hover:ring-pink-200 transition-all">
1195-                                       <div className="flex-1 min-w-0">
--
1229-                                { name: "WRC Oceanside", phone: "(760) 757-3500", desc: "Women's Resource Center", color: "pink" },
1230-                                { name: "N. County LGBTQ", phone: "(760) 994-1690", desc: "Inclusive Support", color: "slate" }
1231:                              ].map((item, i) => (
1232-                                <div key={i} className="p-4 bg-white rounded-2xl border border-slate-100 flex flex-col justify-between hover:ring-2 hover:ring-blue-100 transition-all shadow-sm group">
1233-                                  <div className="mb-4">
--
1368-                          </thead>
1369-                          <tbody className="divide-y divide-[#f1f5f9]">
1370:                            {status.identified_resources.map((m, i) => {
1371-                              const searchUrl = `https://www.google.com/search?q=${encodeURIComponent(`North San Diego County ${m.item} ${m.unit} services availability Oceanside Vista`)}`;
1372-                              const isDetoxOrBed = m.item.toLowerCase().includes('detox') || m.item.toLowerCase().includes('bed');
--
1434-                    
1435-                    <div className="flex gap-2 overflow-x-auto pb-2 scrollbar-none">
1436:                      {(['all', 'safety', 'healing', 'basics', 'healthcare'] as const).map((cat) => (
1437-                        <button
1438-                          key={cat}
--
1455-                           <span className="text-[10px] font-black text-slate-400 uppercase tracking-widest">Optimized for Your Case</span>
1456-                        </div>
1457:                        {geocodedRefs.map((loc, i) => (
1458-                          <div 
1459-                            key={i} 
--
1490-                       {NORTH_COUNTY_RESOURCES
1491-                        .filter(loc => mapFilter === 'all' || loc.type === mapFilter)
1492:                        .map((loc, i) => {
1493-                          const distance = userCoords ? (function(lat1: number, lng1: number, lat2: number, lng2: number) {
1494-                            const R = 6371;
--
1609-                          {NORTH_COUNTY_RESOURCES
1610-                            .filter(loc => mapFilter === 'all' || loc.type === mapFilter)
1611:                            .map(loc => (
1612-                            <HelpMarker 
1613-                              key={loc.id} 
--
1624-                          {geocodedRefs
1625-                            .filter(() => mapFilter === 'all' || mapFilter === 'healing') // AI results are usually healing-related or emergency
1626:                            .map(ref => (
1627-                            <HelpMarker 
1628-                              key={ref.id} 
--
1662-                         {/* Mini Legend Overlay */}
1663-                         <div className="absolute top-6 left-6 p-4 bg-white/80 backdrop-blur-md rounded-3xl border border-white shadow-xl space-y-2 pointer-events-none">
1664:                            {Object.entries(CATEGORY_STYLES).map(([key, style]) => (
1665-                               <div key={key} className="flex items-center gap-2">
1666-                                  <div className="w-2.5 h-2.5 rounded-full" style={{ backgroundColor: style.color }}></div>
--
1696-
1697-                    <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
1698:                      {resourceAlerts.map((alert, i) => (
1699-                        <div key={i} className="group p-6 bg-slate-50/30 border border-slate-100 rounded-2xl hover:bg-white hover:shadow-lg transition-all duration-300">
1700-                          <div className="flex items-center justify-between mb-4">
--
1733-                    </div>
1734-                    <div className="space-y-2">
1735:                       {logs.slice(0, 5).map((log, i) => (
1736-                         <div key={i} className="flex gap-4 items-center">
1737-                            <span className="text-[10px] font-black text-slate-300 w-8">0{i+1}</span>
--
1754-          { id: 'map', icon: MapIcon, label: 'Map' },
1755-          { id: 'system', icon: Activity, label: 'Status' }
1756:        ].map((item) => (
1757-          <button
1758-            key={item.id}

<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Google AI Studio App</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.tsx"></script>
  </body>
</html>
node_modules/
build/
dist/
coverage/
.DS_Store
*.log
.env*
!.env.example
# GEMINI_API_KEY: Required for Gemini AI API calls.
# AI Studio automatically injects this at runtime from user secrets.
# Users configure this via the Secrets panel in the AI Studio UI.
GEMINI_API_KEY=
GOOGLE_MAPS_PLATFORM_KEY=
VITE_GOOGLE_MAPS_API_KEY=

# APP_URL: The URL where this applet is hosted.
# AI Studio automatically injects this at runtime with the Cloud Run service URL.
# Used for self-referential links, OAuth callbacks, and API endpoints.
APP_URL="MY_APP_URL"
