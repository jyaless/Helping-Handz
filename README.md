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

/**
 * @license
 * SPDX-License-Identifier: Apache-2.0
 */

import { useState, useRef, useEffect } from 'react';
import { 
  Activity, 
  Map as MapIcon, 
  Cpu, 
  ShieldAlert, 
  Database, 
  Terminal, 
  Camera, 
  Search, 
  Zap, 
  ShieldCheck,
  Star,
  CheckCircle2,
  AlertCircle,
  ChevronRight,
  RefreshCcw,
  Package,
  Layers,
  Sun,
  Cloud,
  Bird,
  HandHelping,
  Heart,
  FileText,
  MapPin,
  ExternalLink,
  Navigation,
  Crosshair
} from 'lucide-react';
import { motion, AnimatePresence } from 'motion/react';
import Markdown from 'react-markdown';
import { APIProvider, Map, AdvancedMarker, Pin, useMap, useMapsLibrary, InfoWindow, useAdvancedMarkerRef } from '@vis.gl/react-google-maps';
import { processInventory, IMAStatus, ResourceItem, TriageData } from './services/imaService';

const API_KEY = ((import.meta as any).env?.VITE_GOOGLE_MAPS_API_KEY || (import.meta as any).env?.GOOGLE_MAPS_PLATFORM_KEY || '') as string;
const hasValidKey = Boolean(API_KEY) && API_KEY.startsWith('AIza') && API_KEY.length >= 35 && API_KEY.length <= 40;

// Expanded regional centers with categories
const NORTH_COUNTY_RESOURCES = [
  { 
    id: 'bennos', 
    lat: 33.1947, 
    lng: -117.3797, 
    title: "Brother Benno's", 
    desc: "Food, Mail, Laundry & Warm Support", 
    type: 'basics' as const, 
    phone: "(760) 439-1244", 
    address: "3260 Production Ave, Oceanside",
    hours: "Mon-Fri 6:30 AM - 11 AM, Sat 6:30 AM - 10 AM",
    logistics: "Walk-ins welcome for breakfast and hygiene items. Mail service available during morning hours."
  },
  { 
    id: 'breadoflife', 
    lat: 33.1925, 
    lng: -117.3712, 
    title: "Bread of Life", 
    desc: "Emergency Rescue Mission & Shelter", 
    type: 'safety' as const, 
    phone: "(760) 722-0800", 
    address: "1919 Apple St, Oceanside",
    hours: "Office: 10 AM - 4 PM daily. Bed intake: 4 PM - 6 PM",
    logistics: "Requires arrival before 4 PM for bed screening. Bring ID if possible. Dinner served nightly at 6 PM."
  },
  { 
    id: 'vista_clinic', 
    lat: 33.2014, 
    lng: -117.2427, 
    title: "Vista Community Clinic", 
    desc: "Medical & Medi-Cal Application Help", 
    type: 'healthcare' as const, 
    phone: "(760) 631-5000", 
    address: "1000 Vale Terrace Dr, Vista",
    hours: "Mon-Fri 8 AM - 8 PM, Sat 9 AM - 4 PM",
    logistics: "Express walk-in clinic available for urgent medical needs. Case managers on site for insurance enrollment."
  },
  { 
    id: 'mcalister', 
    lat: 33.1906, 
    lng: -117.3671, 
    title: "McAlister Institute", 
    desc: "Substance Abuse Detox & Counseling", 
    type: 'healing' as const, 
    phone: "(760) 721-2781", 
    address: "1733 Mission Ave, Oceanside",
    hours: "24/7 Intake for Detox",
    logistics: "Immediate entry available for medically monitored detox. Please call ahead if possible, but walk-ins accepted."
  },
  { 
    id: 'wrc', 
    lat: 33.1920, 
    lng: -117.3750, 
    title: "Women's Resource Center", 
    desc: "Safe Haven for Women & Families", 
    type: 'safety' as const, 
    phone: "(760) 757-3500", 
    address: "1963 Apple St, Oceanside",
    hours: "Crisis Line: 24/7. Office: 9 AM - 5 PM",
    logistics: "Emergency shelter for domestic violence survivors. Secure location. Call the crisis line first for safety protocols."
  },
  { 
    id: 'interfaith', 
    lat: 33.1972, 
    lng: -117.3592, 
    title: "Interfaith Community Services", 
    desc: "Housing & Veterans Support", 
    type: 'safety' as const, 
    phone: "(760) 721-2117", 
    address: "1617 Mission Ave, Oceanside",
    hours: "Mon-Fri 8 AM - 5 PM",
    logistics: "Veteran services and bridge housing. Mobile outreach teams operate during daylight hours."
  },
  { 
    id: 'tri_city', 
    lat: 33.1868, 
    lng: -117.3005, 
    title: "Tri-City Medical Center", 
    desc: "Emergency Room & Crisis Stabilization", 
    type: 'healthcare' as const, 
    phone: "(760) 724-8411", 
    address: "4002 Vista Way, Oceanside",
    hours: "24/7 Emergency Care",
    logistics: "Designated crisis stabilization unit for mental health emergencies. Accessible via SPRINTER walk from nearby station."
  },
  { 
    id: 'first_step_men', 
    lat: 33.1416, 
    lng: -117.3197, 
    title: "First Step House (Men's)", 
    desc: "Alcohol-Only 10-Day Detox", 
    type: 'healing' as const, 
    phone: "(760) 230-9353", 
    address: "3808 Adams Street, Carlsbad",
    hours: "8 AM - 8 PM Intake",
    logistics: "Alcohol-only sanctuary. Free 10-day introduction to sobriety. Indigent and alcoholic men prioritize. No drugs allowed."
  },
  { 
    id: 'first_step_women', 
    lat: 33.2175, 
    lng: -117.2528, 
    title: "Women's First Step House", 
    desc: "Alcohol-Only 10-Day Detox", 
    type: 'healing' as const, 
    phone: "(760) 542-6724", 
    address: "508 Toucan Dr, Vista",
    hours: "8 AM - 8 PM Intake",
    logistics: "Alcohol-only safe haven for women. Free 10-day stay. Safe and caring environment to build a foundation for recovery."
  }
];

const CATEGORY_STYLES = {
  safety: { color: '#f43f5e', icon: ShieldAlert, label: 'Safe Havens' },  // red-500
  healing: { color: '#8b5cf6', icon: Activity, label: 'Healing' },      // violet-500
  basics: { color: '#f59e0b', icon: Package, label: 'Basic Needs' },     // amber-500
  healthcare: { color: '#3b82f6', icon: Zap, label: 'Medical' },         // blue-500
  user: { color: '#ec4899', icon: MapPin, label: 'You' }                // pink-500
};

// Marker component with InfoCard
function HelpMarker({ position, title, description, type, phone, address, isSuggested }: { 
  position: google.maps.LatLngLiteral, 
  title: string, 
  description: string, 
  type: keyof typeof CATEGORY_STYLES,
  phone?: string,
  address?: string,
  isSuggested?: boolean
}) {
  const [markerRef, marker] = useAdvancedMarkerRef();
  const [infoWindowShown, setInfoWindowShown] = useState(false);
  const style = CATEGORY_STYLES[type];

  return (
    <>
      <AdvancedMarker
        ref={markerRef}
        position={position}
        onClick={() => setInfoWindowShown(true)}
      >
        <div className="relative group">
          {isSuggested && (
            <div className="absolute -top-1 px-1.5 py-0.5 bg-yellow-400 text-white text-[7px] font-black uppercase tracking-widest rounded-full shadow-lg -translate-y-full left-1/2 -translate-x-1/2 mb-1 animate-bounce whitespace-nowrap z-50">
              Pick
            </div>
          )}
          <Pin 
            background={isSuggested ? '#f59e0b' : style.color} 
            borderColor="#fff" 
            glyphColor="#fff" 
            scale={infoWindowShown ? 1.4 : (isSuggested ? 1.25 : 1.1)}
          />
        </div>
      </AdvancedMarker>
      {infoWindowShown && (
        <InfoWindow
          anchor={marker}
          onCloseClick={() => setInfoWindowShown(false)}
        >
          <div className="p-3 max-w-[240px] space-y-2">
            <div className="flex items-center gap-2">
               <div className="p-1 rounded-md bg-slate-50">
                  <style.icon className="w-4 h-4" style={{ color: style.color }} />
               </div>
               <h4 className="font-black text-slate-800 text-sm">{title}</h4>
            </div>
            <p className="text-[11px] text-slate-600 leading-relaxed font-medium italic">"{description}"</p>
            {(phone || address) && (
              <div className="pt-2 mt-2 border-t border-slate-100 flex flex-col gap-1.5">
                 {phone && (
                   <a href={`tel:${phone.replace(/[^0-9]/g, '')}`} className="flex items-center gap-2 text-[10px] font-black text-blue-600 hover:underline">
                      <HandHelping className="w-3 h-3" />
                      {phone}
                   </a>
                 )}
                  {address && (
                   <a 
                     href={`https://www.google.com/maps/dir/?api=1&destination=${encodeURIComponent(address)}`}
                     target="_blank"
                     rel="noreferrer"
                     className="flex items-start gap-2 text-[10px] font-bold text-slate-400 hover:text-blue-600 transition-colors"
                   >
                      <MapPin className="w-3 h-3 mt-0.5" />
                      {address}
                   </a>
                 )}
              </div>
            )}
          </div>
        </InfoWindow>
      )}
    </>
  );
}

// Map Controller for fitsBounds and location updates
function MapController({ center }: { center?: google.maps.LatLngLiteral }) {
  const map = useMap();
  useEffect(() => {
    if (map && center) {
      map.panTo(center);
      map.setZoom(14);
    }
  }, [map, center]);
  return null;
}

export default function App() {
  const [triage, setTriage] = useState<TriageData>({
    gender: 'male',
    primaryChallenge: 'alcohol',
    currentStatus: 'stabilized',
    transportNeeded: false,
    hasInsurance: 'none',
    location: {
      address: '',
      city: '',
      state: 'CA',
      zip: ''
    }
  });
  const [chaosInput, setChaosInput] = useState("");
  const [isProcessing, setIsProcessing] = useState(false);
  const [status, setStatus] = useState<IMAStatus | null>(null);
  const [logs, setLogs] = useState<string[]>(["SYSTEM: Ready to help. Scan your papers or tell us what happened."]);
  const [showToolkit, setShowToolkit] = useState(false);
  const [activeTab, setActiveTab] = useState<'audit' | 'map' | 'directory' | 'system'>('audit');
  const [checkedLogistics, setCheckedLogistics] = useState<Record<string, boolean>>({});
  const [checkedResources, setCheckedResources] = useState<Record<string, boolean>>({});

  // Simulated live resource data for the "Status" tab
  const resourceAlerts = [
    { type: 'bed', level: 'low', title: 'Emergency Beds', msg: 'Bread of Life (Oceanside) reporting 4 beds remaining as of 5:42 AM.', time: '18m ago' },
    { type: 'voucher', level: 'ok', title: 'Transit Vouchers', msg: 'NCTD Breeze bus passes available at Interfaith Mission Ave office.', time: '1h ago' },
    { type: 'safety', level: 'alert', title: 'Weather Advisory', msg: 'Low temperatures expected (48°F). Extra blankets at Brother Benno\'s.', time: '2h ago' },
    { type: 'healing', level: 'ok', title: 'Detox Intake', msg: 'McAlister Institute currently accepting walk-ins for screening until 2PM.', time: '4h ago' }
  ];
  const [userCoords, setUserCoords] = useState<{lat: number, lng: number} | null>(null);
  const [geocodedRefs, setGeocodedRefs] = useState<{id: string, lat: number, lng: number, title: string, desc: string, address?: string}[]>([]);
  const [locationMode, setLocationMode] = useState<'gps' | 'manual' | null>(null);
  const [mapFilter, setMapFilter] = useState<keyof typeof CATEGORY_STYLES | 'all'>('all');
  const [mapError, setMapError] = useState(false);
  const [expandedResourceId, setExpandedResourceId] = useState<string | null>(null);
  
  useEffect(() => {
    (window as any).gm_authFailure = () => {
      setMapError(true);
    };
  }, []);

  const placesLib = useMapsLibrary('places');

  // Geocode AI results when they arrive using local master list
  useEffect(() => {
    if (!status?.references) return;
    
    const newRefs: {id: string, lat: number, lng: number, title: string, desc: string, address?: string}[] = [];
    
    for (const ref of status.references) {
      // Find a fuzzy match in NORTH_COUNTY_RESOURCES
      const match = NORTH_COUNTY_RESOURCES.find(r => 
        ref.name.toLowerCase().includes(r.title.toLowerCase()) || 
        r.title.toLowerCase().includes(ref.name.toLowerCase())
      );
      
      if (match) {
        newRefs.push({
          id: match.id,
          lat: match.lat,
          lng: match.lng,
          title: ref.name,
          desc: ref.phone,
          address: ref.address
        });
      } else {
        // Fallback: If not found, use a slight random offset from Oceanside center
        newRefs.push({
          id: Math.random().toString(),
          lat: 33.1959 + (Math.random() - 0.5) * 0.05,
          lng: -117.3795 + (Math.random() - 0.5) * 0.05,
          title: ref.name,
          desc: ref.phone,
          address: ref.address
        });
      }
    }
    
    setGeocodedRefs(newRefs);
    if (newRefs.length > 0) {
      setUserCoords({ lat: newRefs[0].lat, lng: newRefs[0].lng });
      addLog(`Mapped ${newRefs.length} suggested facilities.`);
    }
  }, [status]);

  const detectLocation = () => {
    if (!navigator.geolocation) {
      addLog("Geolocation is not supported by your browser.");
      return;
    }
    addLog("Detecting location via GPS...");
    navigator.geolocation.getCurrentPosition(
      (position) => {
        const coords = {
          lat: position.coords.latitude,
          lng: position.coords.longitude
        };
        setUserCoords(coords);
        setTriage(t => ({ 
          ...t, 
          location: { 
            ...t.location!, 
            address: 'GPS Detected', 
            city: 'North County', 
            state: 'CA', 
            zip: 'Current' 
          } 
        }));
        addLog(`Located: ${coords.lat.toFixed(4)}, ${coords.lng.toFixed(4)}`);
      },
      (error) => {
        addLog(`Location error: ${error.message}`);
      }
    );
  };
  
  const addLog = (msg: string) => {
    setLogs(prev => [`[${new Date().toLocaleTimeString()}] ${msg}`, ...prev].slice(0, 50));
  };

  const handleAudit = async () => {
    if (!chaosInput.trim()) return;
    
    setIsProcessing(true);
    addLog(`Initiating recovery route mapping...`);
    
    try {
      const result = await processInventory(chaosInput, triage);
      setStatus(result);
      addLog(`Plan generated for Case ${result.node_id}.`);
      addLog(`Next step identified.`);
    } catch (error) {
      addLog("Something went wrong. Please try again or call local support.");
      console.error(error);
    } finally {
      setIsProcessing(false);
    }
  };

  const exampleNotes = [
    "I need immediate detox and medical support assistance.",
    "Searching for safe housing and prenatal medical care options.",
    "In a mental health crisis and need emergency shelter.",
    "Looking for a safe haven for a parent and child.",
    "Seeking assistance with basic needs and housing resources."
  ];

  return (
    <div className="min-h-screen bg-transparent text-[#1e293b] font-sans selection:bg-pink-100 selection:text-pink-900 pb-20 lg:pb-0 relative overflow-hidden">
      {/* Hopeful Background Elements */}
      <div className="fixed inset-0 pointer-events-none z-[-2]">
        {/* Sun */}
        <motion.div 
          initial={{ opacity: 0, scale: 0.8 }}
          animate={{ opacity: 0.2, scale: 1 }}
          transition={{ duration: 2 }}
          className="absolute -top-20 -right-20 w-96 h-96 bg-yellow-100 rounded-full blur-[100px]"
        />
        
        {/* Clouds */}
        <motion.div 
          animate={{ x: [0, 50, 0] }}
          transition={{ duration: 20, repeat: Infinity, ease: "linear" }}
          className="absolute top-[10%] left-[5%] text-blue-100 opacity-30"
        >
          <Cloud className="w-32 h-32" />
        </motion.div>
        
        <motion.div 
          animate={{ x: [0, -40, 0] }}
          transition={{ duration: 25, repeat: Infinity, ease: "linear" }}
          className="absolute top-[40%] right-[10%] text-white opacity-40"
        >
          <Cloud className="w-48 h-48" />
        </motion.div>
 
        {/* Birds */}
        <motion.div 
          initial={{ x: -100, y: 100 }}
          animate={{ x: [0, 1000], y: [0, -100] }}
          transition={{ duration: 60, repeat: Infinity, ease: "linear" }}
          className="absolute bottom-[20%] left-0 text-white opacity-20"
        >
          <Bird className="w-12 h-12" />
        </motion.div>
      </div>
 
      {/* Header */}
      <header className="bg-white/80 backdrop-blur-md border-b border-white/50 px-6 py-4 flex items-center justify-between sticky top-0 z-50 shadow-sm">
        <div className="flex items-center gap-4">
          <div className="p-3 bg-gradient-to-br from-blue-600 to-pink-500 text-white rounded-2xl shadow-xl shadow-blue-100 ring-4 ring-white">
            <HandHelping className="w-6 h-6" />
          </div>
          <div>
            <h1 className="text-xl font-black tracking-tighter text-slate-900 leading-none mb-1">A Helping Hand</h1>
            <p className="text-[9px] text-blue-600 font-black uppercase tracking-[0.2em] hidden sm:block">North County Recovery Guide</p>
          </div>
        </div>
        
        <div className="flex items-center gap-4">
           {/* Tab Selection in Header for Desktop to save space */}
           <div className="hidden md:flex gap-1 bg-white/50 p-1 rounded-xl border border-white/80">
            {[
              { id: 'audit', icon: Search, label: 'Get Help' },
              { id: 'directory', icon: Package, label: 'Resources' },
              { id: 'map', icon: MapIcon, label: 'Map' },
              { id: 'system', icon: Activity, label: 'Status' }
            ].map((item) => (
              <button
                key={item.id}
                onClick={() => setActiveTab(item.id as any)}
                className={`flex items-center gap-2 px-4 py-1.5 rounded-lg transition-all font-bold text-xs ${activeTab === item.id ? 'bg-white text-blue-500 shadow-sm' : 'text-slate-500 hover:bg-white/50'}`}
              >
                <item.icon className="w-3 h-3" />
                {item.label}
              </button>
            ))}
          </div>
        </div>
      </header>
 
      <main className="max-w-6xl mx-auto py-12 px-4 lg:px-6">
        {/* Drifting Clouds Background Layer */}
      <div className="fixed inset-0 pointer-events-none overflow-hidden z-[-1] opacity-40">
        <motion.div 
          animate={{ x: [-200, 1500] }}
          transition={{ duration: 120, repeat: Infinity, ease: "linear" }}
          className="absolute top-[10%] left-[-20%] text-white/60"
        >
          <Cloud className="w-[400px] h-[400px] blur-3xl fill-white" />
        </motion.div>
        <motion.div 
          animate={{ x: [1500, -200] }}
          transition={{ duration: 150, repeat: Infinity, ease: "linear" }}
          className="absolute top-[40%] right-[-20%] text-blue-100/40"
        >
          <Cloud className="w-[500px] h-[500px] blur-3xl fill-blue-50" />
        </motion.div>
        <motion.div 
          animate={{ x: [-300, 1600] }}
          transition={{ duration: 180, repeat: Infinity, ease: "linear", delay: 20 }}
          className="absolute bottom-[10%] left-[-25%] text-pink-100/40"
        >
          <Cloud className="w-[600px] h-[600px] blur-3xl fill-pink-50" />
        </motion.div>
      </div>

      {/* Hero Section */}
        <div className="text-center mb-16 relative">
          <motion.div
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            className="inline-flex items-center gap-3 px-6 py-2 rounded-full bg-white/40 backdrop-blur-md border border-white/60 text-blue-600 font-bold text-xs uppercase tracking-[0.2em] mb-8 shadow-sm"
          >
            Compassion is our Compass
          </motion.div>
          {/* More Clouds */}
        <motion.div 
          animate={{ x: [0, 50, 0], y: [0, -20, 0] }}
          transition={{ duration: 25, repeat: Infinity, ease: "easeInOut" }}
          className="absolute top-1/4 right-[10%] opacity-20 pointer-events-none"
        >
          <Cloud className="w-64 h-64 text-purple-200 fill-purple-100/50" />
        </motion.div>

        <motion.div 
          animate={{ x: [0, -40, 0], y: [0, 30, 0] }}
          transition={{ duration: 30, repeat: Infinity, ease: "easeInOut", delay: 5 }}
          className="absolute bottom-1/4 left-[5%] opacity-15 pointer-events-none"
        >
          <Cloud className="w-80 h-80 text-blue-200 fill-blue-100/50" />
        </motion.div>

        <motion.div 
          animate={{ opacity: [0.1, 0.3, 0.1] }}
          transition={{ duration: 10, repeat: Infinity }}
          className="absolute top-[60%] right-[30%] pointer-events-none"
        >
          <Cloud className="w-32 h-32 text-pink-200 fill-pink-100/30" />
        </motion.div>

        <motion.h1 
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ delay: 0.1 }}
            className="text-5xl md:text-7xl font-black text-slate-900 mb-6 tracking-tight leading-tight"
          >
            Providing a Clear Path
          </motion.h1>
          <motion.div 
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ delay: 0.2 }}
            className="space-y-4"
          >
            <p className="text-2xl md:text-4xl text-blue-600 font-serif italic">Recovery, Housing and Hope</p>
            <p className="text-xl md:text-2xl text-slate-500 font-black uppercase tracking-[0.3em]">North San Diego County</p>
          </motion.div>
        </div>
        
        <div className="relative">
          <AnimatePresence mode="wait">
            {activeTab === 'audit' && (
              <motion.div 
                initial={{ opacity: 0, y: 10 }}
                animate={{ opacity: 1, y: 0 }}
                exit={{ opacity: 0, y: -10 }}
                className="grid grid-cols-1 lg:grid-cols-12 gap-6"
              >
                {/* Left Column: Input and Triage */}
                <div className="lg:col-span-5 space-y-6">
                  
                  {/* Quick Triage Form */}
                  <div className="sturdy-card overflow-hidden">
                    <div className="p-6 border-b-2 border-slate-50 bg-slate-50/30 flex items-center justify-between">
                      <div className="flex items-center gap-3">
                        <div className="w-2.5 h-8 bg-blue-600 rounded-full shadow-[0_0_10px_rgba(37,99,235,0.3)]"></div>
                        <div>
                          <h3 className="font-black text-sm text-slate-900 uppercase tracking-widest">Entry Triage</h3>
                          <p className="text-[10px] text-slate-400 font-bold uppercase tracking-tighter">Vital for resource mapping</p>
                        </div>
                      </div>
                    </div>
                    <div className="p-6 space-y-8">
                      {/* Location Section */}
                      <div className="bg-blue-50/30 p-5 rounded-2xl border-2 border-blue-100/50">
                        <label className="text-[10px] font-black text-blue-600 uppercase mb-4 block tracking-widest text-center">Where can we find you?</label>
                        <div className="grid grid-cols-2 gap-4 mb-4">
                          <button
                            onClick={() => {
                              setLocationMode('gps');
                              setTriage(t => ({ ...t, transportNeeded: true }));
                              detectLocation();
                            }}
                            className={`sturdy-button py-3.5 text-[11px] font-black uppercase border-2 flex items-center justify-center gap-2 ${locationMode === 'gps' ? 'bg-blue-600 text-white border-blue-700 shadow-lg shadow-blue-100' : 'bg-white text-slate-500 border-slate-100 hover:border-blue-200'}`}
                          >
                            <Crosshair className="w-4 h-4" />
                            GPS
                          </button>
                          <button
                            onClick={() => {
                              setLocationMode('manual');
                              setTriage(t => ({ ...t, transportNeeded: true }));
                            }}
                            className={`sturdy-button py-3.5 text-[11px] font-black uppercase border-2 flex items-center justify-center gap-2 ${locationMode === 'manual' ? 'bg-pink-500 text-white border-pink-700 shadow-lg shadow-pink-100' : 'bg-white text-slate-500 border-slate-100 hover:border-pink-200'}`}
                          >
                            <MapPin className="w-4 h-4" />
                            Manual
                          </button>
                        </div>
 
                        <AnimatePresence>
                          {locationMode === 'manual' && (
                            <motion.div 
                              initial={{ opacity: 0, height: 0 }}
                              animate={{ opacity: 1, height: 'auto' }}
                              exit={{ opacity: 0, height: 0 }}
                              className="space-y-3 overflow-hidden pt-2"
                            >
                              <input 
                                type="text" 
                                placeholder="Street Address"
                                value={triage.location?.address}
                                onChange={(e) => setTriage(t => ({ ...t, location: { ...t.location!, address: e.target.value } }))}
                                className="w-full bg-white border-2 border-slate-100 rounded-xl p-4 text-sm font-bold focus:border-blue-400 transition-all outline-none"
                              />
                              <div className="grid grid-cols-2 gap-3">
                                <input 
                                  type="text" 
                                  placeholder="City"
                                  value={triage.location?.city}
                                  onChange={(e) => setTriage(t => ({ ...t, location: { ...t.location!, city: e.target.value } }))}
                                  className="bg-white border-2 border-slate-100 rounded-xl p-4 text-sm font-bold focus:border-blue-400 outline-none"
                                />
                                <input 
                                  type="text" 
                                  placeholder="Zip"
                                  value={triage.location?.zip}
                                  onChange={(e) => setTriage(t => ({ ...t, location: { ...t.location!, zip: e.target.value } }))}
                                  className="bg-white border-2 border-slate-100 rounded-xl p-4 text-sm font-bold focus:border-blue-400 outline-none"
                                />
                              </div>
                            </motion.div>
                          )}
                          {locationMode === 'gps' && (
                            <motion.div 
                              initial={{ opacity: 0 }}
                              animate={{ opacity: 1 }}
                              className="text-center p-3"
                            >
                              <p className="text-[10px] font-black text-blue-500 uppercase tracking-widest flex items-center justify-center gap-2">
                                <div className="w-1.5 h-1.5 bg-blue-500 rounded-full animate-ping"></div>
                                {userCoords ? "GPS Coords Locked" : "Locating..."}
                              </p>
                              {userCoords && (
                                <p className="text-[9px] text-slate-400 mt-1">{userCoords.lat.toFixed(4)}, {userCoords.lng.toFixed(4)}</p>
                              )}
                            </motion.div>
                          )}
                        </AnimatePresence>
                      </div>
 
                      <div>
                        <label className="text-[10px] font-black text-slate-400 uppercase mb-3 block tracking-widest">Insurance Status</label>
                        <div className="grid grid-cols-3 gap-3">
                          {[
                            { id: 'medi_cal', label: 'Medi-Cal' },
                            { id: 'private', label: 'Private' },
                            { id: 'none', label: 'None' }
                          ].map((i) => (
                            <button
                              key={i.id}
                              onClick={() => setTriage(t => ({ ...t, hasInsurance: i.id as any }))}
                              className={`sturdy-button py-3 px-1 text-[10px] font-black uppercase border-2 transition-all ${triage.hasInsurance === i.id ? 'bg-blue-600 text-white border-blue-700' : 'bg-white text-slate-500 border-slate-100 hover:border-blue-200'}`}
                            >
                              {i.label}
                            </button>
                          ))}
                        </div>
                      </div>
 
                      <div>
                        <label className="text-[10px] font-black text-slate-400 uppercase mb-3 block tracking-widest">Identify Gender</label>
                        <div className="grid grid-cols-3 gap-3">
                          {['male', 'female', 'lgbtq+'].map((g) => (
                            <button
                              key={g}
                              onClick={() => setTriage(t => ({ ...t, gender: g.replace('+', '') as any }))}
                              className={`sturdy-button py-3 text-[10px] font-black uppercase border-2 transition-all ${triage.gender === g.replace('+', '') ? 'bg-blue-600 text-white border-blue-700' : 'bg-white text-slate-500 border-slate-100 hover:border-blue-200'}`}
                            >
                              {g}
                            </button>
                          ))}
                        </div>
                      </div>
 
                      <div>
                        <label className="text-[10px] font-black text-slate-400 uppercase mb-3 block tracking-widest">Primary Challenge</label>
                        <div className="grid grid-cols-2 gap-3">
                          {[
                            { id: 'alcohol', label: 'Alcohol Focus' },
                            { id: 'drug_alcohol', label: 'Drugs & Alcohol' },
                            { id: 'mental_health', label: 'Mental Health' },
                            { id: 'housing', label: 'Housing Only' },
                            { id: 'domestic_violence', label: 'Domestic Violence' },
                            { id: 'child_care_pregnancy', label: 'Child Care & Pregnancy' }
                          ].map((c) => (
                            <button
                              key={c.id}
                              onClick={() => setTriage(t => ({ ...t, primaryChallenge: c.id as any }))}
                              className={`sturdy-button py-3.5 px-2 rounded-xl text-[10px] font-black uppercase border-2 transition-all ${triage.primaryChallenge === c.id ? 'bg-blue-600 text-white border-blue-700 shadow-lg shadow-blue-100' : 'bg-white text-slate-500 border-slate-100 hover:border-blue-200'}`}
                            >
                              {c.label}
                            </button>
                          ))}
                        </div>
                      </div>
 
                      <div>
                        <label className="text-[10px] font-black text-slate-400 uppercase mb-3 block tracking-widest">Clinical State</label>
                        <div className="grid grid-cols-2 gap-3">
                          {[
                            { id: 'influence', label: 'Under Influence' },
                            { id: 'detox_needed', label: 'Detox Needed' },
                            { id: 'stabilized', label: 'Stabilized' },
                            { id: 'crisis', label: 'Mental Crisis' }
                          ].map((s) => (
                            <button
                              key={s.id}
                              onClick={() => setTriage(t => ({ ...t, currentStatus: s.id as any }))}
                              className={`sturdy-button py-3.5 px-2 rounded-xl text-[10px] font-black uppercase border-2 transition-all text-center leading-tight ${triage.currentStatus === s.id ? 'bg-blue-600 text-white border-blue-700 shadow-lg shadow-blue-100' : 'bg-white text-slate-500 border-slate-100 hover:border-blue-200'}`}
                            >
                              {s.label}
                            </button>
                          ))}
                        </div>
                      </div>
                    </div>
                  </div>

                  {/* Recovery Toolkit Expansion */}
                  <div className="sturdy-card overflow-hidden bg-gradient-to-br from-purple-50/50 to-pink-50/50">
                    <button 
                      onClick={() => setShowToolkit(!showToolkit)}
                      className="w-full p-6 flex items-center justify-between hover:bg-white/40 transition-all text-left"
                    >
                      <div className="flex items-center gap-4">
                        <div className="w-12 h-12 bg-white rounded-2xl flex items-center justify-center shadow-sm border-2 border-purple-100">
                          <Zap className="w-6 h-6 text-purple-500" />
                        </div>
                        <div>
                          <h3 className="font-black text-sm text-slate-900 uppercase tracking-widest">Recovery Toolkit</h3>
                          <p className="text-[10px] text-purple-600 font-black uppercase tracking-tighter">Tools to help you find focus</p>
                        </div>
                      </div>
                      <ChevronRight className={`w-5 h-5 text-purple-400 transition-transform ${showToolkit ? 'rotate-90' : ''}`} />
                    </button>

                    <AnimatePresence>
                      {showToolkit && (
                        <motion.div
                          initial={{ height: 0, opacity: 0 }}
                          animate={{ height: 'auto', opacity: 1 }}
                          exit={{ height: 0, opacity: 0 }}
                          className="px-6 pb-8 space-y-6 overflow-hidden"
                        >
                          <div className="h-[2px] bg-white/60"></div>
                          
                          {/* Focus & Localization Strategy */}
                          <div className="space-y-4">
                            <h4 className="text-[10px] font-black text-purple-500 uppercase tracking-widest flex items-center gap-2">
                              <Crosshair className="w-3 h-3" />
                              Regional Grounding (Localized)
                            </h4>
                            <div className="grid grid-cols-1 gap-3">
                              <div className="p-5 bg-white/80 rounded-2xl border-2 border-white shadow-sm space-y-3">
                                <p className="text-[10px] font-black text-slate-400 uppercase tracking-widest">Sense Alignment</p>
                                <ul className="space-y-4">
                                  <li className="flex items-start gap-3">
                                    <div className="w-5 h-5 bg-blue-100 rounded-full flex items-center justify-center shrink-0 mt-0.5">
                                      <Sun className="w-3 h-3 text-blue-600" />
                                    </div>
                                    <p className="text-[11px] font-bold text-slate-700 leading-relaxed italic">
                                      "Breathe in the salt air if you're near the coast in Oceanside or Carlsbad. Feel the ocean breeze—it's been crossing thousand of miles just to reach you."
                                    </p>
                                  </li>
                                  <li className="flex items-start gap-3">
                                    <div className="w-5 h-5 bg-amber-100 rounded-full flex items-center justify-center shrink-0 mt-0.5">
                                      <Bird className="w-3 h-3 text-amber-600" />
                                    </div>
                                    <p className="text-[11px] font-bold text-slate-700 leading-relaxed italic">
                                      "Look at the rolling hills of Vista or the peaks in San Marcos. Those same hills have watched over people finding their way for generations. You are not alone in this landscape."
                                    </p>
                                  </li>
                                  <li className="flex items-start gap-3">
                                    <div className="w-5 h-5 bg-rose-100 rounded-full flex items-center justify-center shrink-0 mt-0.5">
                                      <Heart className="w-3 h-3 text-rose-600" />
                                    </div>
                                    <p className="text-[11px] font-bold text-slate-700 leading-relaxed italic">
                                      "Find a physical object: a palm frond, a pebble from a hiking trail, or even the feeling of your feet on the sidewalk. This ground is North County and it is solid beneath you."
                                    </p>
                                  </li>
                                </ul>
                              </div>
                            </div>
                          </div>

                          {/* Quick Checklist */}
                          <div className="space-y-4">
                            <h4 className="text-[10px] font-black text-blue-500 uppercase tracking-widest flex items-center gap-2">
                              <CheckCircle2 className="w-3 h-3" />
                              The "Get" List
                            </h4>
                            <div className="bg-white/80 rounded-3xl p-6 border-2 border-white space-y-1">
                              {[
                                { item: "Physical ID (DL or State ID)", priority: "Critical" },
                                { item: "Social Security Number (on paper)", priority: "High" },
                                { item: "3 Days worth of Meds (if any)", priority: "Critical" },
                                { item: "Phone Charger", priority: "Helpful" },
                                { item: "Clean Socks (2 pair)", priority: "Essential" }
                              ].map((check, idx) => (
                                <button 
                                  key={idx} 
                                  onClick={() => setCheckedResources(prev => ({ ...prev, [check.item]: !prev[check.item] }))}
                                  className={`w-full flex items-center justify-between py-3 px-3 rounded-xl transition-all border-b border-transparent ${checkedResources[check.item] ? 'bg-emerald-50/30' : 'hover:bg-slate-50'}`}
                                >
                                  <div className="flex items-center gap-3">
                                    <div className={`w-5 h-5 rounded-md border-2 flex items-center justify-center transition-colors ${checkedResources[check.item] ? 'border-emerald-500 bg-emerald-500' : 'border-blue-200 bg-white'}`}>
                                      {checkedResources[check.item] && <CheckCircle2 className="w-3.5 h-3.5 text-white" />}
                                    </div>
                                    <span className={`text-xs font-bold ${checkedResources[check.item] ? 'text-emerald-700' : 'text-slate-700'}`}>{check.item}</span>
                                  </div>
                                  <span className={`text-[8px] font-black uppercase px-2 py-0.5 rounded-full ${
                                    checkedResources[check.item] ? 'bg-emerald-100 text-emerald-600' :
                                    check.priority === 'Critical' ? 'bg-red-50 text-red-500' : 
                                    check.priority === 'High' ? 'bg-orange-50 text-orange-500' : 'bg-blue-50 text-blue-500'
                                  }`}>
                                    {checkedResources[check.item] ? 'Obtained' : check.priority}
                                  </span>
                                </button>
                              ))}
                            </div>
                          </div>

                          {/* Structure Section */}
                          <div className="p-5 bg-indigo-600 rounded-3xl text-white shadow-xl shadow-indigo-100">
                            <h4 className="text-[10px] font-black uppercase tracking-[0.2em] mb-3 flex items-center gap-2">
                              <ShieldCheck className="w-4 h-4 text-indigo-200" />
                              Establishing Structure
                            </h4>
                            <p className="text-xs font-medium leading-relaxed mb-4">
                              Recovery thrives on routine. Even if you are on the street tonight, set three anchors:
                            </p>
                            <ul className="space-y-2">
                              <li className="text-[11px] font-black flex items-center gap-3 bg-white/10 p-3 rounded-xl border border-white/10">
                                <span className="text-indigo-200">01</span> AWAKE BY 7:00 AM
                              </li>
                              <li className="text-[11px] font-black flex items-center gap-3 bg-white/10 p-3 rounded-xl border border-white/10">
                                <span className="text-indigo-200">02</span> HYDRATE IMMEDIATELY
                              </li>
                              <li className="text-[11px] font-black flex items-center gap-3 bg-white/10 p-3 rounded-xl border border-white/10">
                                <span className="text-indigo-200">03</span> CHECK-IN WITH 1 PERSON
                              </li>
                            </ul>
                          </div>
                        </motion.div>
                      )}
                    </AnimatePresence>
                  </div>
 
                  <div className="flex justify-center my-12 relative z-10">
                    <motion.div 
                      animate={{ rotate: 360 }}
                      transition={{ duration: 20, repeat: Infinity, ease: 'linear' }}
                      className="bg-white p-4 rounded-full border border-orange-100 shadow-xl shadow-orange-50 relative"
                    >
                      <Sun className="w-12 h-12 text-orange-400 fill-orange-100" />
                      <div className="absolute inset-0 flex items-center justify-center">
                        <div className="w-2 h-2 bg-white rounded-full"></div>
                      </div>
                    </motion.div>
                  </div>
 
                  {/* Manual Story */}
                  <div className="sturdy-card overflow-hidden">
                    <div className="p-4 border-b-2 border-slate-50 bg-white flex items-center justify-between">
                      <div className="flex items-center gap-2">
                        <FileText className="w-4 h-4 text-blue-500" />
                        <h3 className="font-extrabold text-[10px] text-slate-800 uppercase tracking-widest">Share Your Story</h3>
                        <Bird className="w-4 h-4 text-blue-300 ml-1" />
                      </div>
                    </div>
                    <textarea 
                      value={chaosInput}
                      onChange={(e) => setChaosInput(e.target.value)}
                      placeholder="Tell us about your current situation or select a starting point below..."
                      className="w-full h-32 bg-transparent p-5 text-sm font-medium focus:outline-none resize-none placeholder:text-slate-300 border-none"
                    />
                    <div className="px-5 pb-5 flex flex-wrap gap-2">
                      <button 
                        onClick={() => setChaosInput("")}
                        className="text-[10px] px-3 py-1 bg-white border-2 border-blue-600 rounded-lg font-black text-blue-600 hover:bg-blue-50 transition-all shadow-sm uppercase tracking-tighter"
                      >
                        Write My Own
                      </button>
                      {exampleNotes.map((note, i) => (
                        <button 
                          key={i}
                          onClick={() => setChaosInput(note)}
                          className="text-[10px] px-3 py-1 bg-slate-50 border-2 border-slate-100 rounded-lg font-black text-slate-400 hover:bg-blue-50 hover:text-blue-500 hover:border-blue-100 transition-all shadow-sm uppercase tracking-tighter"
                        >
                          Scenario {i+1}
                        </button>
                      ))}
                    </div>
                  </div>

                  {/* Action Button Container */}
                  <div className="space-y-4">
                    <button 
                      onClick={handleAudit}
                      disabled={isProcessing || !chaosInput.trim()}
                      className="sturdy-button w-full py-6 bg-blue-600 text-white font-black text-sm uppercase border-blue-800 disabled:opacity-30 disabled:cursor-not-allowed flex items-center justify-center gap-3"
                    >
                      {isProcessing ? (
                        <>
                          <RefreshCcw className="w-5 h-5 animate-spin" />
                          Mapping your path...
                        </>
                      ) : (
                        <>
                          <Sun className="w-6 h-6 fill-white/20" />
                          Open My Path to Healing
                        </>
                      )}
                    </button>
                    <p className="text-[10px] text-center text-slate-400 font-black uppercase tracking-[0.2em] px-8">
                       Propelled by Gemini 1.5 Flash Intelligence
                    </p>
                  </div>
                </div>

                {/* Right Column: Results */}
                <div className="lg:col-span-7 space-y-6">
                  {/* Plan Output */}
                  <div className="sturdy-card overflow-hidden min-h-[400px] flex flex-col">
                    <div className="p-4 border-b-2 border-slate-50 bg-white flex items-center justify-between">
                      <div className="flex items-center gap-2">
                        <Terminal className="w-4 h-4 text-blue-500" />
                        <h3 className="font-extrabold text-[10px] text-slate-800 uppercase tracking-widest italic">Compassion Roadmap</h3>
                      </div>
                    </div>
                    
                    <div className="flex-1 p-8">
                      {status ? (
                        <motion.div 
                          initial={{ opacity: 0 }} 
                          animate={{ opacity: 1 }}
                          className="space-y-8"
                        >
                          {/* Procedural Integrity Indicator */}
                          <div className="mb-12 bg-slate-50/50 p-8 rounded-3xl border border-slate-100 flex items-center gap-6 shadow-sm">
                            <div className="w-16 h-16 bg-white rounded-2xl flex items-center justify-center shrink-0 border border-slate-100 shadow-sm">
                              <ShieldCheck className="w-8 h-8 text-blue-600" />
                            </div>
                            <div>
                              <h5 className="text-slate-900 font-bold text-sm uppercase tracking-widest mb-1">Logistics Integrity</h5>
                              <p className="text-[11px] text-slate-500 font-medium leading-relaxed">
                                Strategy verified against regional infrastructure. Use the call buttons below to confirm real-time bed and voucher availability before travel.
                              </p>
                            </div>
                          </div>

                          {/* Main Plan Area */}
                          <div className="p-6 md:p-12 bg-white rounded-3xl border border-slate-200 shadow-xl relative overflow-hidden">
                            <div className="relative z-10 max-w-2xl mx-auto">
                              <div className="flex flex-col items-center mb-8 text-center border-b border-slate-100 pb-6">
                                <h4 className="font-sans font-black text-xl text-slate-900 mb-1 uppercase tracking-tight">
                                  Action Plan & Logistics
                                </h4>
                                <p className="text-[10px] text-slate-400 font-bold uppercase tracking-[0.2em]">Step-by-step guidance for your situation</p>
                              </div>

                              <div className="prose prose-slate max-w-none 
                                prose-h3:text-slate-930 prose-h3:font-black prose-h3:uppercase prose-h3:tracking-widest prose-h3:text-sm prose-h3:mt-10 prose-h3:mb-6 prose-h3:pb-2 prose-h3:border-b prose-h3:border-slate-100
                                prose-p:text-sm prose-p:leading-relaxed prose-p:text-slate-500 prose-p:mb-4 prose-p:font-medium
                                prose-ul:pl-0 prose-ul:space-y-1
                                prose-strong:text-slate-800 prose-strong:font-black
                                prose-em:text-slate-400 prose-em:font-bold prose-em:not-italic prose-em:text-[10px]
                              ">
                                <Markdown
                                  components={{
                                    li: ({ children }) => {
                                      const findText = (node: any): string => {
                                        if (typeof node === 'string') return node;
                                        if (Array.isArray(node)) return node.map(findText).join(' ');
                                        if (node?.props?.children) return findText(node.props.children);
                                        return '';
                                      };
                                      const text = findText(children);
                                      const normalizedText = text.toLowerCase();
                                      const isChecked = checkedLogistics[text] || false;
                                      
                                      const getCityStyle = (t: string) => {
                                        if (t.includes('oceanside')) return { style: 'border-blue-100 text-blue-900 bg-blue-50/30', dot: 'border-blue-400', label: 'Oceanside' };
                                        if (t.includes('vista')) return { style: 'border-violet-100 text-violet-900 bg-violet-50/30', dot: 'border-violet-400', label: 'Vista' };
                                        if (t.includes('carlsbad')) return { style: 'border-amber-100 text-amber-900 bg-amber-50/30', dot: 'border-amber-400', label: 'Carlsbad' };
                                        if (t.includes('escondido')) return { style: 'border-indigo-100 text-indigo-900 bg-indigo-50/30', dot: 'border-indigo-400', label: 'Escondido' };
                                        if (t.includes('san marcos')) return { style: 'border-rose-100 text-rose-900 bg-rose-50/30', dot: 'border-rose-400', label: 'San Marcos' };
                                        return { style: 'border-slate-100 text-slate-700 bg-white', dot: 'border-slate-300', label: null };
                                      };

                                      const city = getCityStyle(normalizedText);

                                      return (
                                        <li 
                                          onClick={() => setCheckedLogistics(prev => ({ ...prev, [text]: !prev[text] }))}
                                          className={`list-none flex items-center gap-4 p-4 rounded-2xl border-2 mb-2 cursor-pointer select-none transition-all duration-300 group
                                            ${isChecked 
                                              ? 'bg-emerald-50 border-emerald-200' 
                                              : `hover:bg-opacity-100 ${city.style}`}`}
                                        >
                                          <div className="shrink-0 flex items-center justify-center">
                                            {isChecked ? (
                                              <CheckCircle2 className="w-6 h-6 text-emerald-500 fill-emerald-50" />
                                            ) : (
                                              <div className={`w-6 h-6 rounded-full border-2 transition-colors ${city.dot} group-hover:bg-slate-100`} />
                                            )}
                                          </div>
                                          <div className={`flex-1 text-sm font-bold leading-tight ${isChecked ? 'text-emerald-900' : ''}`}>
                                            {children}
                                          </div>
                                          {city.label && !isChecked && (
                                            <span className="text-[8px] font-black uppercase tracking-widest px-2 py-0.5 rounded-full bg-white/80 border border-current/10 opacity-70">
                                              {city.label}
                                            </span>
                                          )}
                                        </li>
                                      );
                                    }
                                  }}
                                >
                                  {status.action_plan}
                                </Markdown>
                              </div>

                              <div className="mt-12 pt-8 border-t border-slate-100 text-center">
                                <p className="text-[10px] font-bold text-slate-400 uppercase tracking-widest italic">
                                  This document is for logistics and information purposes. Factual accuracy is prioritized over rhetoric.
                                </p>
                              </div>
                            </div>
                          </div>

                          {/* Proximity Alignment Section (New) */}
                          {userCoords && status.references && status.references.length > 0 && (
                            <div className="bg-white p-6 rounded-3xl border-2 border-blue-50 shadow-sm space-y-4">
                              <div className="flex items-center justify-between">
                                <h4 className="text-[10px] font-black text-blue-600 uppercase tracking-[0.2em] flex items-center gap-2">
                                  <Navigation className="w-3 h-3" />
                                  Proximity Alignment
                                </h4>
                                <span className="text-[9px] font-black text-slate-400 uppercase tracking-widest bg-slate-50 px-2 py-0.5 rounded-full">
                                  Calculated via {locationMode === 'gps' ? 'GPS' : 'Input'}
                                </span>
                              </div>
                              
                              {/* Calculate and sort by proximity */}
                              <div className="space-y-3">
                                {status.references
                                  .map(ref => {
                                    // Try to find geocoded coords for this reference
                                    const geo = geocodedRefs.find(g => g.title === ref.name);
                                    // Fallback to static resource coords if names match
                                    const staticMatch = NORTH_COUNTY_RESOURCES.find(s => s.title === ref.name);
                                    
                                    const targetLat = geo?.lat || staticMatch?.lat;
                                    const targetLng = geo?.lng || staticMatch?.lng;
                                    
                                    const dist = (targetLat && targetLng && userCoords) ? (function(lat1: number, lng1: number, lat2: number, lng2: number) {
                                      const R = 6371;
                                      const dLat = (lat2 - lat1) * Math.PI / 180;
                                      const dLng = (lng2 - lng1) * Math.PI / 180;
                                      const a = Math.sin(dLat / 2) * Math.sin(dLat / 2) + Math.cos(lat1 * Math.PI / 180) * Math.cos(lat2 * Math.PI / 180) * Math.sin(dLng / 2) * Math.sin(dLng / 2);
                                      const c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1 - a));
                                      return R * c;
                                    })(userCoords.lat, userCoords.lng, targetLat, targetLng) : null;

                                    return { ...ref, dist, targetLat, targetLng };
                                  })
                                  .filter(ref => ref.dist !== null)
                                  .sort((a, b) => (a.dist || 0) - (b.dist || 0))
                                  .map((ref, idx) => (
                                    <div key={idx} className="flex items-center justify-between p-4 bg-slate-50/50 rounded-2xl border border-slate-100 group hover:border-blue-200 transition-colors">
                                      <div className="flex-1 min-w-0">
                                        <p className="font-black text-slate-900 text-xs truncate uppercase tracking-tight">{ref.name}</p>
                                        <p className="text-[10px] text-slate-500 font-bold flex items-center gap-1">
                                          <MapPin className="w-2.5 h-2.5" />
                                          {ref.dist! < 1 ? 'Under 1 km' : `${ref.dist!.toFixed(1)} km`} away
                                        </p>
                                      </div>
                                      <div className="flex gap-2">
                                        {ref.targetLat && ref.targetLng && (
                                          <button 
                                            onClick={() => {
                                              setUserCoords({ lat: ref.targetLat!, lng: ref.targetLng! });
                                              setActiveTab('map');
                                            }}
                                            className="p-2 bg-white text-blue-500 rounded-xl border border-blue-100 shadow-sm hover:bg-blue-50 transition-colors"
                                            title="View on Map"
                                          >
                                            <MapIcon className="w-4 h-4" />
                                          </button>
                                        )}
                                        <a 
                                          href={`https://www.google.com/maps/dir/?api=1&destination=${encodeURIComponent(ref.address)}`}
                                          target="_blank"
                                          rel="noreferrer"
                                          className="flex items-center gap-2 px-4 py-2 bg-blue-600 text-white rounded-xl text-[10px] font-black uppercase shadow-lg shadow-blue-100"
                                        >
                                          <Navigation className="w-3 h-3" />
                                          Go
                                        </a>
                                      </div>
                                    </div>
                                  ))}
                              </div>
                            </div>
                          )}

                          {/* Reference Section (New) */}
                          {status.references && status.references.length > 0 && (
                            <div className="space-y-4">
                              <div className="flex items-center justify-between px-2">
                                <h4 className="text-[#0f172a] font-extrabold text-[12px] uppercase tracking-widest flex items-center gap-2 px-2">
                                  <Database className="w-3.5 h-3.5 text-blue-500" />
                                  Primary Resource Options
                                </h4>
                                <a 
                                  href={`https://www.google.com/search?q=${encodeURIComponent(`North San Diego County ${triage.primaryChallenge} recovery resources Oceanside Vista Escondido`)}`}
                                  target="_blank"
                                  rel="noreferrer"
                                  className="text-[9px] font-black uppercase text-blue-500 bg-blue-50 px-2 py-1 rounded-full border border-blue-100 flex items-center gap-1 hover:bg-blue-100 transition-all"
                                >
                                  <Search className="w-2.5 h-2.5" />
                                  Expand Search Results
                                </a>
                              </div>
                              <div className="grid grid-cols-1 md:grid-cols-2 gap-3">
                                {status.references.map((ref, idx) => (
                                  <div key={idx} className="p-4 bg-white/60 backdrop-blur-sm rounded-xl border border-white group hover:border-pink-300 transition-all shadow-sm">
                                    <div className="flex justify-between items-start mb-2">
                                      <p className="font-extrabold text-slate-800 text-sm">{ref.name}</p>
                                      {!triage.transportNeeded && (
                                        <a 
                                          href={`https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(`${ref.name} ${ref.address}`)}`}
                                          target="_blank"
                                          rel="noreferrer"
                                          className="p-1.5 bg-blue-50 text-blue-500 rounded-lg hover:bg-blue-100 transition-colors"
                                          title="Open in Google Maps"
                                        >
                                          <MapIcon className="w-3 h-3" />
                                        </a>
                                      )}
                                    </div>
                                    <div className="space-y-1.5">
                                      <div className="flex items-center gap-2 text-[11px] text-blue-500 font-bold">
                                        <ChevronRight className="w-3 h-3" />
                                        <a href={`tel:${ref.phone.replace(/[^0-9]/g, '')}`}>{ref.phone}</a>
                                      </div>
                                      <div className="flex items-start gap-2 text-[10px] text-slate-500 leading-tight">
                                        <MapIcon className="w-3 h-3 shrink-0 mt-0.5" />
                                        {ref.address}
                                      </div>
                                      {ref.website && (
                                        <div className="flex items-center gap-2 text-[10px] text-pink-500 font-bold mt-2 truncate">
                                          <ExternalLink className="w-3 h-3" />
                                          {ref.website.replace('https://', '')}
                                        </div>
                                      )}
                                    </div>
                                  </div>
                                ))}
                              </div>
                            </div>
                          )}

                          {/* Backup Options Section (New) */}
                          {status.backup_options && status.backup_options.length > 0 && (
                            <div className="space-y-4 pt-6 mt-6 border-t border-slate-100">
                               <div className="bg-pink-50/50 p-4 rounded-2xl border border-pink-100">
                                 <h4 className="text-pink-600 font-extrabold text-[10px] uppercase tracking-widest flex items-center gap-2 mb-2">
                                   <ShieldAlert className="w-3 h-3" />
                                   Next Best Options (Backup)
                                 </h4>
                                 <p className="text-[10px] text-slate-500 font-medium italic mb-4 leading-relaxed">
                                   If the primary locations above are full or unavailable, we strongly recommend calling these centers immediately. Some prioritize phone check-ins over online listings.
                                 </p>
                                 <div className="grid grid-cols-1 gap-2">
                                   {status.backup_options.map((backup, i) => (
                                     <div key={i} className="bg-white/80 p-3 rounded-xl border border-white shadow-sm flex items-center justify-between gap-4 group hover:ring-2 hover:ring-pink-200 transition-all">
                                       <div className="flex-1 min-w-0">
                                         <p className="text-xs font-black text-slate-800 truncate uppercase tracking-tight">{backup.name}</p>
                                         <p className="text-[9px] text-slate-500 font-medium leading-tight">{backup.reason_to_call}</p>
                                       </div>
                                       <a 
                                         href={`tel:${backup.phone.replace(/[^0-9]/g, '')}`}
                                         className="flex items-center gap-2 px-3 py-1.5 bg-pink-500 text-white rounded-lg text-[10px] font-black uppercase shadow-lg shadow-pink-100 group-hover:bg-pink-600 transition-all"
                                       >
                                         <HandHelping className="w-3 h-3" />
                                         Call Now
                                       </a>
                                     </div>
                                   ))}
                                 </div>
                               </div>
                            </div>
                          )}

                          {/* Manual Resource Directory (Statics) */}
                          <div className="pt-12 space-y-6">
                            <div className="flex items-center gap-4">
                              <div className="h-[2px] flex-1 bg-slate-100"></div>
                              <h4 className="text-slate-400 font-extrabold text-[11px] uppercase tracking-[0.3em] flex items-center gap-2 whitespace-nowrap">
                                <MapIcon className="w-4 h-4" />
                                24/7 NORTH COUNTY SUPPORT
                              </h4>
                              <div className="h-[2px] flex-1 bg-slate-100"></div>
                            </div>
                            <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
                              {[
                                { name: "2-1-1 San Diego", phone: "211", desc: "Housing & Vital Resources", color: "blue" },
                                { name: "McAlister Institute", phone: "(760) 721-2781", desc: "Regional Detox Intake", color: "pink" },
                                { name: "ACCESS Line", phone: "(888) 724-7240", desc: "Mental Health Crisis", color: "slate" },
                                { name: "988 Lifeline", phone: "988", desc: "Suicide & Crisis Help", color: "blue" },
                                { name: "WRC Oceanside", phone: "(760) 757-3500", desc: "Women's Resource Center", color: "pink" },
                                { name: "N. County LGBTQ", phone: "(760) 994-1690", desc: "Inclusive Support", color: "slate" }
                              ].map((item, i) => (
                                <div key={i} className="p-4 bg-white rounded-2xl border border-slate-100 flex flex-col justify-between hover:ring-2 hover:ring-blue-100 transition-all shadow-sm group">
                                  <div className="mb-4">
                                    <p className="text-[11px] font-black text-slate-900 uppercase tracking-tight mb-1">{item.name}</p>
                                    <p className="text-[10px] text-slate-500 font-medium leading-tight">{item.desc}</p>
                                  </div>
                                  <a 
                                    href={`tel:${item.phone.replace(/[^0-9]/g, '')}`} 
                                    className={`text-xs font-black py-2 rounded-lg text-center transition-all ${
                                      item.color === 'blue' ? 'bg-blue-50 text-blue-600 hover:bg-blue-100' :
                                      item.color === 'pink' ? 'bg-pink-50 text-pink-600 hover:bg-pink-100' :
                                      'bg-slate-50 text-slate-600 hover:bg-slate-100'
                                    }`}
                                  >
                                    {item.phone}
                                  </a>
                                </div>
                              ))}
                            </div>
                          </div>
                          
                          <div className="pt-2 border-t border-slate-100">
                            <div className="flex justify-between items-center mb-2 px-1">
                              <span className="text-[10px] font-black text-slate-400 uppercase tracking-tighter">Compassion Alignment Confidence</span>
                              <span className="text-sm font-black text-blue-500">{(status.confidence_score * 100).toFixed(0)}%</span>
                            </div>
                            <div className="w-full bg-slate-100 h-3 rounded-full overflow-hidden shadow-inner">
                              <motion.div 
                                initial={{ width: 0 }}
                                animate={{ width: `${status.confidence_score * 100}%` }}
                                className="h-full bg-blue-400 shadow-[0_0_12px_rgba(96,165,250,0.4)]" 
                              />
                            </div>
                          </div>
                        </motion.div>
                      ) : isProcessing ? (
                        <div className="h-full flex flex-col items-center justify-center gap-6 py-12">
                          <motion.div 
                            animate={{ rotate: 360 }}
                            transition={{ duration: 2, repeat: Infinity, ease: "linear" }}
                            className="w-16 h-16 text-[#4f46e5]"
                          >
                             <RefreshCcw className="w-full h-full" />
                          </motion.div>
                          <div className="text-center max-w-sm">
                            <p className="text-lg font-black text-[#0f172a] uppercase tracking-tight">Synthesizing Route...</p>
                            <p className="text-sm text-[#64748b] font-medium leading-relaxed">
                              Gemini 1.5 Flash is cross-referencing your clinical state with verified available beds in North San Diego County.
                            </p>
                          </div>
                        </div>
                      ) : (
                        <div className="h-full flex flex-col items-center justify-center gap-5 py-12 opacity-30 grayscale saturate-0">
                          <Activity className="w-20 h-20 text-[#cbd5e1]" />
                          <div className="text-center">
                            <p className="text-lg font-black text-[#64748b] uppercase tracking-widest">Awaiting Triage Input</p>
                            <p className="text-xs text-[#94a3b8] font-bold uppercase mt-2">Complete the forms to your left to map your route.</p>
                          </div>
                        </div>
                      )}
                    </div>
                  </div>

                  {/* Info Panel: Community Compass */}
                  <div className={`bg-gradient-to-br transition-all duration-500 ${triage.transportNeeded ? 'from-pink-400 to-blue-300' : 'from-blue-400 to-pink-300'} rounded-3xl p-8 text-white shadow-xl relative overflow-hidden group`}>
                    <div className="absolute top-0 right-0 w-64 h-64 bg-white/10 rounded-full -mr-20 -mt-20 blur-3xl group-hover:bg-white/20 transition-all duration-700"></div>
                    <div className="flex items-center justify-between mb-6">
                      <div className="flex items-center gap-4">
                        <div className="w-10 h-10 bg-white/20 rounded-xl flex items-center justify-center backdrop-blur-md">
                          <MapIcon className="w-5 h-5 text-white" />
                        </div>
                        <h3 className="font-black text-sm uppercase tracking-[0.2em]">Community Compass</h3>
                      </div>
                      {triage.transportNeeded && (
                        <div className="px-3 py-1 bg-white/20 rounded-full backdrop-blur-md border border-white/30 text-[10px] font-black uppercase tracking-tighter">
                          Transport Mode Active
                        </div>
                      )}
                    </div>
                    
                    <div className="grid grid-cols-1 md:grid-cols-2 gap-6 relative z-10">
                      {triage.transportNeeded ? (
                        <>
                          <div className="space-y-2">
                            <p className="text-[10px] font-bold text-white/80 uppercase tracking-widest">Navigation Assistance</p>
                            <p className="text-sm font-medium leading-snug">Input your location above. We will provide literal street-level directions for your journey.</p>
                          </div>
                          <div className="space-y-2">
                            <p className="text-[10px] font-bold text-white/80 uppercase tracking-widest">Ride Support</p>
                            <p className="text-sm font-medium leading-snug">Vouchers for BREEZE buses and SPRINTER rail are available at Brother Benno's in Oceanside.</p>
                          </div>
                        </>
                      ) : (
                        <>
                          <div className="space-y-2">
                            <p className="text-[10px] font-bold text-white/80 uppercase tracking-widest">Self-Navigation</p>
                            <p className="text-sm font-medium leading-snug">Verified resources mapped below. Tap the map icon to open navigation on your phone.</p>
                          </div>
                          <div className="space-y-2">
                            <p className="text-[10px] font-bold text-white/80 uppercase tracking-widest">Local Transit</p>
                            <p className="text-sm font-medium leading-snug">The SPRINTER rail line connects all key recovery points between Oceanside and Escondido.</p>
                          </div>
                        </>
                      )}
                      
                      <div className="col-span-full pt-4 border-t border-white/10 text-center">
                         <div className="inline-flex items-center gap-3 bg-white/10 px-4 py-2 rounded-full backdrop-blur-sm">
                            <div className="w-2 h-2 rounded-full bg-white animate-pulse"></div>
                            <p className="text-[10px] font-black uppercase tracking-[0.1em]">
                              {triage.transportNeeded ? "Your path is being mapped line by line." : "Verified Map links provided with results."}
                            </p>
                         </div>
                      </div>
                    </div>
                  </div>

                  {/* Resource List */}
                  {status && (
                    <motion.div 
                      initial={{ opacity: 0, y: 10 }}
                      animate={{ opacity: 1, y: 0 }}
                      className="bg-white rounded-2xl border border-[#e2e8f0] overflow-hidden shadow-sm"
                    >
                      <div className="p-4 border-b border-[#f1f5f9] bg-slate-50">
                        <div className="flex items-center gap-2">
                          <Cloud className="w-4 h-4 text-blue-300" />
                          <h3 className="font-extrabold text-xs text-slate-800 uppercase tracking-wide">Resources Identified</h3>
                        </div>
                      </div>
                      <div className="overflow-x-auto">
                        <table className="w-full text-left">
                          <thead>
                            <tr className="border-b border-[#f1f5f9] text-[#64748b] uppercase text-[9px] font-black bg-slate-50">
                              <th className="px-6 py-4">Security Asset</th>
                              <th className="px-6 py-4 text-right">Value/Qty</th>
                              <th className="px-6 py-4">State</th>
                            </tr>
                          </thead>
                          <tbody className="divide-y divide-[#f1f5f9]">
                            {(status.identified_resources || []).map((m, i) => {
                              const searchUrl = `https://www.google.com/search?q=${encodeURIComponent(`North San Diego County ${m.item} ${m.unit} services availability Oceanside Vista`)}`;
                              const isDetoxOrBed = m.item.toLowerCase().includes('detox') || m.item.toLowerCase().includes('bed');
                              const isObtained = checkedResources[m.item] || false;
                              
                              return (
                                <tr 
                                  key={i} 
                                  className={`hover:bg-slate-50/50 transition-colors cursor-pointer group ${isObtained ? 'bg-emerald-50/30' : ''}`}
                                  onClick={() => setCheckedResources(prev => ({ ...prev, [m.item]: !prev[m.item] }))}
                                >
                                  <td className="px-6 py-4">
                                    <div className="flex items-center gap-4">
                                      <div className={`w-5 h-5 rounded-md border-2 flex items-center justify-center shrink-0 transition-colors ${isObtained ? 'bg-emerald-500 border-emerald-500' : 'border-slate-200 group-hover:border-blue-400'}`}>
                                        {isObtained && <CheckCircle2 className="w-3.5 h-3.5 text-white" />}
                                      </div>
                                      <a 
                                        href={searchUrl}
                                        target="_blank"
                                        rel="noreferrer"
                                        onClick={(e) => e.stopPropagation()}
                                        className={`text-xs font-black uppercase flex items-center gap-2 hover:underline ${isObtained ? 'text-emerald-700' : (isDetoxOrBed ? 'text-red-600' : 'text-[#0f172a]')}`}
                                      >
                                        {m.item}
                                        <ExternalLink className="w-2.5 h-2.5 opacity-40" />
                                      </a>
                                    </div>
                                  </td>
                                  <td className="px-6 py-4 text-right">
                                    <p className={`text-xs font-black font-mono ${isObtained ? 'text-emerald-600' : 'text-blue-500'}`}>{m.quantity} {m.unit}</p>
                                  </td>
                                  <td className="px-6 py-4">
                                    <span className={`inline-flex items-center px-2.5 py-1 rounded-md text-[10px] font-black uppercase border ${isObtained ? 'bg-emerald-100 text-emerald-700 border-emerald-200' : (m.state === 'idle' ? 'bg-pink-50 text-pink-700 border-pink-100' : 'bg-slate-50 text-slate-400 border-slate-100')}`}>
                                      {isObtained ? 'Obtained' : (m.state === 'idle' ? 'Available' : 'Reserved')}
                                    </span>
                                  </td>
                                </tr>
                              );
                            })}
                          </tbody>
                        </table>
                      </div>
                    </motion.div>
                  )}
                </div>
              </motion.div>
            )}

            {activeTab === 'directory' && (
              <motion.div 
                initial={{ opacity: 0 }}
                animate={{ opacity: 1 }}
                exit={{ opacity: 0 }}
                className="max-w-4xl mx-auto space-y-8"
              >
                {/* Search & Filter Header */}
                <div className="bg-white/90 backdrop-blur-xl p-8 rounded-3xl border border-slate-200 shadow-xl">
                  <div className="flex flex-col md:flex-row md:items-center justify-between gap-6">
                    <div>
                      <h3 className="text-2xl font-black text-slate-900 mb-2 uppercase tracking-tight">
                        Resource Directory
                      </h3>
                      <p className="text-xs text-slate-400 font-bold uppercase tracking-widest pl-1">Verified Hubs in North County</p>
                    </div>
                    
                    <div className="flex gap-2 overflow-x-auto pb-2 scrollbar-none">
                      {(['all', 'safety', 'healing', 'basics', 'healthcare'] as const).map((cat) => (
                        <button
                          key={cat}
                          onClick={() => setMapFilter(cat)}
                          className={`px-4 py-2 rounded-xl text-[10px] font-black uppercase tracking-tighter transition-all whitespace-nowrap ${mapFilter === cat ? 'bg-slate-900 text-white' : 'bg-slate-50 text-slate-400 hover:bg-slate-100'}`}
                        >
                          {cat}
                        </button>
                      ))}
                    </div>
                  </div>
                </div>

                <div className="space-y-4">
                   {/* AI Mapped Results Section if any */}
                   {geocodedRefs.length > 0 && mapFilter === 'all' && (
                     <div className="space-y-3 mb-8">
                        <div className="flex items-center gap-2 px-2">
                           <Zap className="w-3" />
                           <span className="text-[10px] font-black text-slate-400 uppercase tracking-widest">Optimized for Your Case</span>
                        </div>
                        {geocodedRefs.map((loc, i) => (
                          <div 
                            key={i} 
                            className="w-full flex items-start gap-4 p-5 bg-gradient-to-br from-yellow-50/30 to-white border border-yellow-100 rounded-3xl transition-all group"
                          >
                             <div className="w-12 h-12 bg-yellow-400 text-white rounded-2xl flex items-center justify-center shrink-0 shadow-lg shadow-yellow-100">
                                <Star className="w-6 h-6" />
                             </div>
                             <div className="flex-1 min-w-0">
                                <p className="font-black text-slate-900 text-sm">{loc.title}</p>
                                <p className="text-[11px] text-yellow-700 font-bold italic leading-tight mt-1 mb-3">{loc.desc || 'Directly identified in your recovery plan.'}</p>
                                <div className="flex gap-2">
                                  <button 
                                    onClick={() => {
                                      setUserCoords({ lat: loc.lat, lng: loc.lng });
                                      setActiveTab('map');
                                    }}
                                    className="px-3 py-1.5 bg-yellow-500 text-white rounded-lg text-[10px] font-black uppercase tracking-tighter"
                                  >
                                    Show Map
                                  </button>
                                  <a href={`tel:${loc.desc?.replace(/[^0-9]/g, '')}`} className="px-3 py-1.5 bg-white border border-yellow-200 text-yellow-700 rounded-lg text-[10px] font-black uppercase tracking-tighter">
                                    Call Now
                                  </a>
                                </div>
                             </div>
                          </div>
                        ))}
                     </div>
                   )}

                   {/* Static Resources */}
                   <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
                       {NORTH_COUNTY_RESOURCES
                        .filter(loc => mapFilter === 'all' || loc.type === mapFilter)
                        .map((loc, i) => {
                          const distance = userCoords ? (function(lat1: number, lng1: number, lat2: number, lng2: number) {
                            const R = 6371;
                            const dLat = (lat2 - lat1) * Math.PI / 180;
                            const dLng = (lng2 - lng1) * Math.PI / 180;
                            const a = Math.sin(dLat / 2) * Math.sin(dLat / 2) + Math.cos(lat1 * Math.PI / 180) * Math.cos(lat2 * Math.PI / 180) * Math.sin(dLng / 2) * Math.sin(dLng / 2);
                            const c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1 - a));
                            return R * c;
                          })(userCoords.lat, userCoords.lng, loc.lat, loc.lng) : null;

                          return (
                          <div key={i} className="flex flex-col bg-white border border-slate-200 rounded-3xl p-6 shadow-sm hover:shadow-md transition-shadow group">
                            <div className="flex items-start gap-4 mb-4">
                              <div className="w-12 h-12 rounded-2xl flex items-center justify-center shrink-0" style={{ backgroundColor: `${CATEGORY_STYLES[loc.type].color}15`, color: CATEGORY_STYLES[loc.type].color }}>
                                  {(() => {
                                    const Icon = CATEGORY_STYLES[loc.type].icon;
                                    return <Icon className="w-6 h-6" />;
                                  })()}
                              </div>
                              <div className="flex-1 min-w-0">
                                  <div className="flex items-center justify-between gap-2 overflow-hidden">
                                    <p className="font-black text-slate-900 text-sm truncate">{loc.title}</p>
                                    {distance !== null && (
                                      <span className="text-[9px] font-black text-blue-500 bg-blue-50 px-2 py-0.5 rounded-full border border-blue-100 whitespace-nowrap">
                                        {distance < 1 ? '<1 km' : `${distance.toFixed(1)} km`}
                                      </span>
                                    )}
                                  </div>
                                  <p className="text-[11px] text-slate-500 font-bold leading-tight mt-1">{loc.desc}</p>
                              </div>
                            </div>
                            
                            <div className="space-y-3 mt-auto">
                              <p className="text-[10px] text-slate-400 font-medium leading-relaxed line-clamp-2 italic">
                                "{loc.logistics}"
                              </p>
                              <div className="pt-2 flex flex-wrap gap-2">
                                <button 
                                  onClick={() => {
                                    setUserCoords({ lat: loc.lat, lng: loc.lng });
                                    setActiveTab('map');
                                  }}
                                  className="flex items-center gap-2 px-3 py-2 bg-slate-50 rounded-xl text-[10px] font-black uppercase text-slate-600 border border-slate-100"
                                >
                                   <MapIcon className="w-3 h-3" />
                                   Map
                                </button>
                                <a 
                                  href={`tel:${loc.phone.replace(/[^0-9]/g, '')}`}
                                  className="flex items-center gap-2 px-3 py-2 bg-blue-600 rounded-xl text-[10px] font-black uppercase text-white shadow-lg shadow-blue-100"
                                >
                                   <HandHelping className="w-3 h-3" />
                                   Call
                                </a>
                              </div>
                            </div>
                          </div>
                          );
                        })}
                   </div>
                </div>
              </motion.div>
            )}

            {activeTab === 'map' && (
              <motion.div 
                initial={{ opacity: 0 }}
                animate={{ opacity: 1 }}
                exit={{ opacity: 0 }}
                className="h-[800px] lg:h-[700px] bg-white/40 backdrop-blur-xl rounded-[3rem] border-4 border-white shadow-inner relative overflow-hidden"
              >
                  {!hasValidKey || mapError ? (
                    <div className="absolute inset-0 flex flex-col items-center justify-center p-12 text-center bg-white/95 backdrop-blur-xl z-20">
                      <div className="w-24 h-24 bg-pink-50 text-pink-500 rounded-[2rem] flex items-center justify-center mb-8 shadow-inner ring-8 ring-pink-50/50">
                        <MapPin className="w-12 h-12" />
                      </div>
                      <h2 className="text-3xl font-serif italic text-slate-900 mb-6 font-black">Valid Google Maps Key Needed</h2>
                      <div className="max-w-md text-sm text-slate-700 space-y-6 text-left bg-white p-8 rounded-[2rem] border-2 border-slate-50 shadow-2xl">
                        <p className="font-bold text-slate-500 uppercase tracking-widest text-[10px]">Setup Required</p>
                        <p className="leading-relaxed">To provide accurate navigation and mapping, please provide a valid API key:</p>
                        <ol className="list-decimal list-inside space-y-4 font-black text-slate-800">
                          <li>Get an API Key from the <a href="https://console.cloud.google.com/google/maps-apis/start" target="_blank" rel="noopener" className="text-blue-600 underline text-[12px]">Google Maps Platform Console</a>.</li>
                          <li>Open the <strong>Settings</strong> (⚙️) menu in the top right, then select <strong>Secrets</strong>.</li>
                          <li>Add a new secret named <code>VITE_GOOGLE_MAPS_API_KEY</code>.</li>
                          <li>Paste your key and save. The map will load automatically.</li>
                        </ol>
                        <div className="pt-4 border-t border-slate-50 flex items-center gap-3">
                           <RefreshCcw className="w-4 h-4 text-blue-500 animate-spin-slow" />
                           <p className="text-[10px] text-slate-400 italic font-medium">The map will bloom to life as soon as a valid key is provided.</p>
                        </div>
                      </div>
                    </div>
                  ) : (
                    <APIProvider apiKey={API_KEY} solutionChannel="GMP_GCC_reactrecovery_v1" onLoad={() => setMapError(false)}>
                      <div className="w-full h-full">
                        <Map
                          defaultCenter={{ lat: 33.1959, lng: -117.3795 }} // Oceanside CA center
                          defaultZoom={13}
                          mapId="RECOVERY_MAP_STURDY"
                          gestureHandling={'greedy'}
                          disableDefaultUI={true}
                          internalUsageAttributionIds={['gmp_mcp_codeassist_v1_aistudio']}
                          style={{ width: '100%', height: '100%' }}
                        >
                          <MapController center={userCoords || undefined} />
                          
                          {/* User Location */}
                          {userCoords && (
                            <HelpMarker 
                              position={userCoords} 
                              title="Your Location" 
                              description="Detected via GPS" 
                              type="user" 
                            />
                          )}

                          {/* Static Resources */}
                          {NORTH_COUNTY_RESOURCES
                            .filter(loc => mapFilter === 'all' || loc.type === mapFilter)
                            .map(loc => (
                            <HelpMarker 
                              key={loc.id} 
                              position={{ lat: loc.lat, lng: loc.lng }} 
                              title={loc.title} 
                              description={loc.desc} 
                              type={loc.type}
                              phone={loc.phone}
                              address={loc.address}
                            />
                          ))}

                          {/* AI Suggested Results */}
                          {geocodedRefs
                            .filter(() => mapFilter === 'all' || mapFilter === 'healing') // AI results are usually healing-related or emergency
                            .map(ref => (
                            <HelpMarker 
                              key={ref.id} 
                              position={{ lat: ref.lat, lng: ref.lng }} 
                              title={ref.title} 
                              description={ref.desc} 
                              type="healing" // Yellow/violet for AI suggestions
                              phone={ref.desc}
                              address={ref.address}
                              isSuggested={true}
                            />
                          ))}
                        </Map>

                        {/* Floating Interaction Controls */}
                        <div className="absolute bottom-10 left-1/2 -translate-x-1/2 flex gap-3 z-30">
                           <button 
                             onClick={detectLocation}
                             className="flex items-center gap-3 p-4 px-6 bg-slate-900 text-white rounded-3xl shadow-2xl border border-white/10 hover:bg-slate-800 transition-all active:scale-95 group font-black uppercase text-[10px] tracking-widest"
                           >
                             <div className="p-1 bg-white/10 rounded-lg group-hover:scale-110 transition-transform">
                                <Crosshair className="w-4 h-4" />
                             </div>
                             Recenter me
                           </button>
                           <button 
                             onClick={() => setUserCoords(null)}
                             className="flex items-center gap-3 p-4 px-6 bg-white text-slate-800 rounded-3xl shadow-2xl border border-slate-100 hover:bg-slate-50 transition-all active:scale-95 group font-black uppercase text-[10px] tracking-widest"
                           >
                             <div className="p-1 bg-slate-100 rounded-lg group-hover:scale-110 transition-transform">
                                <Navigation className="w-4 h-4" />
                             </div>
                             Clear Focus
                           </button>
                        </div>

                         {/* Mini Legend Overlay */}
                         <div className="absolute top-6 left-6 p-4 bg-white/80 backdrop-blur-md rounded-3xl border border-white shadow-xl space-y-2 pointer-events-none">
                            {Object.entries(CATEGORY_STYLES).map(([key, style]) => (
                               <div key={key} className="flex items-center gap-2">
                                  <div className="w-2.5 h-2.5 rounded-full" style={{ backgroundColor: style.color }}></div>
                                  <span className="text-[10px] font-black text-slate-500 uppercase tracking-tighter">{style.label}</span>
                               </div>
                            ))}
                         </div>
                      </div>
                    </APIProvider>
                  )}
              </motion.div>
            )}

            {activeTab === 'system' && (
              <motion.div 
                initial={{ opacity: 0, y: 20 }}
                animate={{ opacity: 1, y: 0 }}
                exit={{ opacity: 0 }}
                className="max-w-4xl mx-auto space-y-8"
              >
                 {/* Live Status Dashboard */}
                 <div className="bg-white p-8 md:p-12 rounded-3xl border border-slate-200 shadow-xl relative overflow-hidden">
                    <div className="flex items-center justify-between mb-10 border-b border-slate-100 pb-8">
                      <div>
                        <h3 className="text-2xl font-black text-slate-900 mb-1 uppercase tracking-tight">Regional Resource Status</h3>
                        <p className="text-[10px] text-slate-400 font-bold uppercase tracking-widest">Network Update • North San Diego County</p>
                      </div>
                      <div className="flex items-center gap-2 px-4 py-2 bg-slate-50 rounded-full border border-slate-100">
                        <div className="w-2 h-2 bg-blue-500 rounded-full animate-pulse transition-all"></div>
                        <span className="text-[10px] font-black text-slate-600 uppercase tracking-widest">Data Normalized</span>
                      </div>
                    </div>

                    <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
                      {resourceAlerts.map((alert, i) => (
                        <div key={i} className="group p-6 bg-slate-50/30 border border-slate-100 rounded-2xl hover:bg-white hover:shadow-lg transition-all duration-300">
                          <div className="flex items-center justify-between mb-4">
                            <span className={`px-2 py-1 rounded text-[8px] font-black uppercase tracking-widest ${
                              alert.level === 'alert' ? 'bg-red-50 text-red-600' : 
                              alert.level === 'low' ? 'bg-amber-50 text-amber-600' : 'bg-slate-100 text-slate-600'
                            }`}>
                              {alert.title}
                            </span>
                            <span className="text-[9px] text-slate-300 font-bold">{alert.time}</span>
                          </div>
                          <p className="text-sm text-slate-700 font-medium leading-relaxed">{alert.msg}</p>
                        </div>
                      ))}
                    </div>

                    <div className="mt-12 p-8 bg-slate-50 rounded-2xl border border-slate-100 relative overflow-hidden">
                       <div className="flex items-start gap-4 relative z-10">
                          <div className="p-3 bg-white rounded-xl border border-slate-200 text-slate-400 shadow-sm">
                             <Activity className="w-5 h-5" />
                          </div>
                          <div>
                             <p className="text-[10px] font-black text-slate-900 mb-1 uppercase tracking-widest">Operational Disclaimer</p>
                             <p className="text-[11px] text-slate-500 font-medium leading-relaxed max-w-xl">
                               Data points are sourced from regional facility reports. Bed availability and voucher funding are highly volatile. This interface provides estimated status; physical verification via phone call or outreach visit is required for high-stakes transitions.
                             </p>
                          </div>
                       </div>
                    </div>
                 </div>

                 {/* Activity Heartbeat (Condensed) */}
                 <div className="bg-white/40 backdrop-blur-md rounded-[2rem] border border-white p-8 shadow-sm">
                    <div className="flex items-center gap-4 mb-6">
                       <h2 className="text-sm font-black text-slate-900 uppercase tracking-widest">System Activity</h2>
                    </div>
                    <div className="space-y-2">
                       {logs.slice(0, 5).map((log, i) => (
                         <div key={i} className="flex gap-4 items-center">
                            <span className="text-[10px] font-black text-slate-300 w-8">0{i+1}</span>
                            <p className="text-[11px] text-slate-500 font-medium">{log}</p>
                         </div>
                       ))}
                    </div>
                 </div>
              </motion.div>
            )}
          </AnimatePresence>
        </div>
      </main>

      {/* Simplified Footer Navigation for Mobile */}
      <footer className="lg:hidden fixed bottom-0 left-0 right-0 bg-white border-t border-[#e2e8f0] p-2 flex justify-around z-50">
        {[
          { id: 'audit', icon: Search, label: 'Help' },
          { id: 'directory', icon: Package, label: 'Resources' },
          { id: 'map', icon: MapIcon, label: 'Map' },
          { id: 'system', icon: Activity, label: 'Status' }
        ].map((item) => (
          <button
            key={item.id}
            onClick={() => setActiveTab(item.id as any)}
            className={`flex flex-col items-center p-2 rounded-lg transition-all ${activeTab === item.id ? 'text-blue-500' : 'text-slate-400'}`}
          >
            <item.icon className="w-5 h-5" />
            <span className="text-[10px] font-bold mt-1 uppercase tracking-tighter">{item.label}</span>
          </button>
        ))}
      </footer>

      {/* Decorative Gradients */}
      <div className="fixed inset-0 pointer-events-none z-[-2] opacity-30">
        <div className="absolute top-[10%] right-[10%] w-96 h-96 bg-blue-100/50 rounded-full blur-3xl"></div>
        <div className="absolute bottom-[10%] left-[10%] w-96 h-96 bg-pink-100/50 rounded-full blur-3xl"></div>
      </div>
    </div>
  );
}
