import React, { useState, useEffect, useMemo } from 'react';
import { 
  Layout, 
  BarChart3, 
  Users, 
  Calendar, 
  Settings, 
  ChevronRight, 
  Download, 
  Cloud, 
  ShieldCheck, 
  Zap, 
  DollarSign,
  Clock,
  Briefcase,
  Menu,
  X,
  Bell,
  ArrowUpRight,
  Github,
  Globe,
  Database,
  Link as LinkIcon,
  CheckCircle2,
  Loader2,
  RefreshCcw
} from 'lucide-react';

// --- CLOUD CONFIGURATION ---
const CLOUD_CONFIG = {
  API_KEY: "sb_publishable_5jDhRntX09PD8DoNPDGx-g_a5oLt_c6",
  ANON_TOKEN: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InducHdqeXZvenpqeGhsdnVwa2RiIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NzQ5NTQyODAsImV4cCI6MjA5MDUzMDI4MH0.8Zk7sd_S5oIjpdOs7DGy3YkN9OIXvSws8i7_L7WjABg",
  PROJECT_REF: "wnpwjyvovzzjhluvkpdb",
  BASE_URL: "https://wnpwjyvovzzjhluvkpdb.supabase.co"
};

const APP_NAME = "BizFlow OS";

const styles = {
  glass: "bg-white/10 backdrop-blur-md border border-white/20",
  card: "bg-white dark:bg-slate-900 rounded-2xl shadow-sm border border-slate-200 dark:border-slate-800 p-6 transition-all hover:shadow-md",
  buttonPrimary: "bg-indigo-600 hover:bg-indigo-700 text-white font-semibold py-3 px-6 rounded-xl transition-all transform hover:scale-[1.02] active:scale-[0.98] flex items-center gap-2 disabled:opacity-50",
  buttonSecondary: "bg-slate-100 dark:bg-slate-800 hover:bg-slate-200 dark:hover:bg-slate-700 text-slate-900 dark:text-white font-semibold py-3 px-6 rounded-xl transition-all flex items-center gap-2",
  navLink: (isActive) => `flex items-center gap-3 p-3 rounded-lg transition-all cursor-pointer ${isActive ? 'bg-indigo-600 text-white shadow-lg shadow-indigo-500/30' : 'text-slate-600 dark:text-slate-400 hover:bg-indigo-50 dark:hover:bg-slate-800 hover:text-indigo-600'}`
};

// --- SUB-COMPONENTS ---

const StatCard = ({ title, value, change, icon: Icon, trend }) => (
  <div className={styles.card}>
    <div className="flex justify-between items-start mb-4">
      <div className="p-3 bg-indigo-100 dark:bg-indigo-900/30 rounded-xl text-indigo-600">
        <Icon size={24} />
      </div>
      <span className={`text-xs font-bold px-2 py-1 rounded-full ${trend === 'up' ? 'bg-emerald-100 text-emerald-700' : 'bg-rose-100 text-rose-700'}`}>
        {change}
      </span>
    </div>
    <h3 className="text-slate-500 dark:text-slate-400 text-sm font-medium">{title}</h3>
    <p className="text-2xl font-bold text-slate-900 dark:text-white mt-1">{value}</p>
  </div>
);

const DeploymentGenerator = () => {
  const [target, setTarget] = useState('aws');
  const [isExporting, setIsExporting] = useState(false);
  const [progress, setProgress] = useState(0);

  const manifest = useMemo(() => ({
    docker: `FROM node:20-alpine\nWORKDIR /app\nCOPY . .\nRUN npm install\nENV SUPABASE_KEY=${CLOUD_CONFIG.API_KEY}\nRUN npm run build\nEXPOSE 3000\nCMD ["npm", "start"]`,
    github: `name: Cloud-Deploy\non: [push]\njobs:\n  deploy:\n    runs-on: ubuntu-latest\n    env:\n      DB_KEY: \${{ secrets.SUPABASE_KEY }}\n    steps:\n      - uses: actions/checkout@v4\n      - name: Build & Push to ${target.toUpperCase()}\n        run: echo "Deploying via ${CLOUD_CONFIG.PROJECT_REF}..."`
  }), [target]);

  const handleExport = () => {
    setIsExporting(true);
    setProgress(0);
    const interval = setInterval(() => {
      setProgress(prev => {
        if (prev >= 100) {
          clearInterval(interval);
          setTimeout(() => setIsExporting(false), 1000);
          return 100;
        }
        return prev + 5;
      });
    }, 100);
  };

  return (
    <div className="space-y-4">
      <div className="flex gap-4 mb-4">
        {['aws', 'google', 'azure'].map(cloud => (
          <button 
            key={cloud}
            onClick={() => setTarget(cloud)}
            className={`px-4 py-2 rounded-lg capitalize border transition-all ${target === cloud ? 'bg-indigo-600 border-indigo-600 text-white' : 'border-slate-300 dark:border-slate-700'}`}
          >
            {cloud}
          </button>
        ))}
      </div>
      <div className="relative group">
        <pre className="p-4 bg-slate-950 text-emerald-400 rounded-lg text-xs overflow-x-auto border border-slate-800 max-h-48">
          <code>{manifest.docker}</code>
        </pre>
        <div className="absolute top-2 right-2 opacity-0 group-hover:opacity-100 transition-opacity">
          <span className="text-[10px] bg-slate-800 text-slate-300 px-2 py-1 rounded">Auto-Generated</span>
        </div>
      </div>

      {isExporting ? (
        <div className="space-y-2">
          <div className="flex justify-between text-xs font-bold uppercase tracking-wider text-slate-500">
            <span>Compiling Production Build...</span>
            <span>{progress}%</span>
          </div>
          <div className="w-full bg-slate-200 dark:bg-slate-800 h-2 rounded-full overflow-hidden">
            <div className="bg-indigo-600 h-full transition-all duration-300" style={{ width: `${progress}%` }}></div>
          </div>
        </div>
      ) : (
        <button 
          onClick={handleExport}
          className="w-full bg-emerald-600 hover:bg-emerald-700 text-white py-4 rounded-xl font-bold flex justify-center items-center gap-2 transition-transform active:scale-[0.98]"
        >
          <Download size={20} /> Generate Deployment Bundle
        </button>
      )}
    </div>
  );
};

export default function App() {
  const [view, setView] = useState('landing');
  const [sidebarOpen, setSidebarOpen] = useState(true);
  const [isMobileMenuOpen, setIsMobileMenuOpen] = useState(false);
  const [scrolled, setScrolled] = useState(false);

  useEffect(() => {
    const handleScroll = () => setScrolled(window.scrollY > 20);
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  }, []);

  const navigate = (to) => {
    setView(to);
    setIsMobileMenuOpen(false);
    window.scrollTo(0, 0);
  };

  if (view === 'landing') {
    return (
      <div className="min-h-screen bg-white dark:bg-slate-950 text-slate-900 dark:text-white">
        <nav className={`fixed w-full z-[60] transition-all duration-300 ${scrolled ? 'bg-white/90 dark:bg-slate-950/90 backdrop-blur-md py-4 shadow-xl border-b border-slate-200 dark:border-slate-800' : 'bg-transparent py-6'}`}>
          <div className="max-w-7xl mx-auto px-6 flex justify-between items-center">
            <div className="flex items-center gap-2 text-2xl font-black tracking-tighter text-indigo-600 cursor-pointer" onClick={() => navigate('landing')}>
              <Zap fill="currentColor" /> {APP_NAME}
            </div>
            <div className="hidden md:flex items-center gap-8 font-semibold">
              <a href="#features" className="hover:text-indigo-600 transition-colors">Features</a>
              <button onClick={() => navigate('dashboard')} className="bg-indigo-600 text-white px-8 py-3 rounded-full font-bold hover:bg-indigo-700 transition-all shadow-lg shadow-indigo-500/20">
                Launch System
              </button>
            </div>
            <button className="md:hidden p-2" onClick={() => setIsMobileMenuOpen(!isMobileMenuOpen)}>
              {isMobileMenuOpen ? <X /> : <Menu />}
            </button>
          </div>
        </nav>

        {/* Mobile Nav Overlay */}
        {isMobileMenuOpen && (
          <div className="fixed inset-0 z-[55] bg-white dark:bg-slate-950 pt-32 px-6 flex flex-col gap-6 text-2xl font-bold">
            <div onClick={() => navigate('dashboard')} className="flex items-center justify-between">Launch Dashboard <ChevronRight /></div>
            <a href="#features" onClick={() => setIsMobileMenuOpen(false)}>Features</a>
            <div className="pt-6 border-t border-slate-100 dark:border-slate-800">
               <p className="text-sm text-slate-500">Connected to Cloud</p>
               <p className="text-xs font-mono text-emerald-500">ID: {CLOUD_CONFIG.PROJECT_REF}</p>
            </div>
          </div>
        )}

        <section className="pt-48 pb-32 px-6 relative overflow-hidden">
          <div className="absolute top-0 left-1/2 -translate-x-1/2 w-[800px] h-[800px] bg-indigo-500/10 rounded-full blur-[120px] -z-10"></div>
          <div className="max-w-5xl mx-auto text-center">
            <div className="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-indigo-50 dark:bg-indigo-900/30 text-indigo-600 dark:text-indigo-400 font-bold mb-8 border border-indigo-100 dark:border-indigo-800">
              <RefreshCcw size={14} className="animate-spin" /> GitHub-SaaS Sync v2.6
            </div>
            <h1 className="text-5xl md:text-8xl font-black mb-8 tracking-tight leading-[1.1]">
              Scale Your Business <br /> <span className="text-indigo-600">Without the Effort.</span>
            </h1>
            <p className="text-lg md:text-xl text-slate-500 dark:text-slate-400 mb-12 max-w-2xl mx-auto leading-relaxed">
              The only business automation system that converts directly into a portable cloud asset. Own your code, own your data, grow your revenue.
            </p>
            <div className="flex flex-col sm:flex-row gap-4 justify-center">
              <button onClick={() => navigate('dashboard')} className={styles.buttonPrimary}>
                Open Workspace <ChevronRight size={20} />
              </button>
              <button className={styles.buttonSecondary}>
                Watch Technical Demo
              </button>
            </div>
          </div>
        </section>

        <section id="features" className="py-24 bg-slate-50 dark:bg-slate-900/40">
           <div className="max-w-7xl mx-auto px-6 grid md:grid-cols-3 gap-8">
              {[
                { title: "Universal Deployment", desc: "One-click generation of Docker and GitHub Actions for any cloud provider.", icon: Cloud },
                { title: "Automated Billing", desc: "Never manually invoice again. System handles payment triggers automatically.", icon: DollarSign },
                { title: "Encrypted Storage", desc: "Your database is hardened with enterprise-grade tokens and API security.", icon: ShieldCheck }
              ].map((f, i) => (
                <div key={i} className={styles.card}>
                  <div className="w-12 h-12 bg-indigo-600 text-white rounded-xl flex items-center justify-center mb-6 shadow-xl shadow-indigo-500/20">
                    <f.icon size={24} />
                  </div>
                  <h3 className="text-xl font-bold mb-3">{f.title}</h3>
                  <p className="text-slate-600 dark:text-slate-400 leading-relaxed text-sm">{f.desc}</p>
                </div>
              ))}
           </div>
        </section>
      </div>
    );
  }

  return (
    <div className="flex h-screen bg-slate-50 dark:bg-slate-950 text-slate-900 dark:text-white overflow-hidden">
      {/* Dynamic Sidebar */}
      <aside className={`transition-all duration-300 ${sidebarOpen ? 'w-72' : 'w-20'} bg-white dark:bg-slate-900 border-r border-slate-200 dark:border-slate-800 flex flex-col z-50`}>
        <div className="p-6 flex items-center gap-3">
          <div className="w-10 h-10 bg-indigo-600 rounded-xl flex items-center justify-center text-white shrink-0 shadow-lg shadow-indigo-500/30">
            <Zap size={24} fill="white" />
          </div>
          {sidebarOpen && <span className="font-black text-xl tracking-tighter">BIZFLOW</span>}
        </div>

        <nav className="flex-1 px-4 space-y-2 mt-4">
          <div onClick={() => navigate('dashboard')} className={styles.navLink(view === 'dashboard')}>
            <Layout size={20} /> {sidebarOpen && "Overview"}
          </div>
          <div onClick={() => navigate('clients')} className={styles.navLink(view === 'clients')}><Users size={20} /> {sidebarOpen && "Clients"}</div>
          <div onClick={() => navigate('projects')} className={styles.navLink(view === 'projects')}><Briefcase size={20} /> {sidebarOpen && "Projects"}</div>
          <div onClick={() => navigate('finances')} className={styles.navLink(view === 'finances')}><DollarSign size={20} /> {sidebarOpen && "Finances"}</div>
          <div onClick={() => navigate('settings')} className={styles.navLink(view === 'settings')}>
            <Settings size={20} /> {sidebarOpen && "Cloud Core"}
          </div>
        </nav>

        <div className="p-4 border-t border-slate-200 dark:border-slate-800">
           <button onClick={() => setSidebarOpen(!sidebarOpen)} className="w-full flex items-center gap-3 p-3 text-slate-400 hover:text-indigo-600 transition-colors">
             {sidebarOpen ? <X size={20} /> : <Menu size={20} />} {sidebarOpen && "Collapse"}
           </button>
           <button onClick={() => navigate('landing')} className="w-full mt-2 text-[10px] uppercase font-bold text-slate-400 hover:text-rose-500 text-center tracking-widest">
             Exit to Public Web
           </button>
        </div>
      </aside>

      {/* Workspace */}
      <main className="flex-1 overflow-y-auto p-4 md:p-8 relative">
        <header className="flex justify-between items-center mb-8">
          <div>
            <h2 className="text-2xl md:text-3xl font-bold capitalize">{view.replace('_', ' ')}</h2>
            <p className="text-slate-400 text-sm font-medium flex items-center gap-2">
               <span className="w-2 h-2 bg-emerald-500 rounded-full animate-pulse"></span> Live Cloud Sync Active
            </p>
          </div>
          <div className="flex items-center gap-4">
             <div className="hidden sm:flex flex-col text-right">
                <span className="text-xs font-bold text-slate-500">Instance ID</span>
                <span className="text-[10px] font-mono text-indigo-500 uppercase">{CLOUD_CONFIG.PROJECT_REF}</span>
             </div>
             <div className="w-10 h-10 rounded-xl bg-slate-200 dark:bg-slate-800 flex items-center justify-center text-slate-500 cursor-pointer hover:text-indigo-600">
               <Bell size={20} />
             </div>
          </div>
        </header>

        {view === 'dashboard' ? (
          <div className="space-y-8 animate-in fade-in slide-in-from-bottom-4 duration-500">
            <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
              <StatCard title="Global Revenue" value="$142,300" change="+12.4%" icon={DollarSign} trend="up" />
              <StatCard title="Active Assets" value="28" change="+4" icon={Briefcase} trend="up" />
              <StatCard title="Client Sentiment" value="98%" change="+2%" icon={Users} trend="up" />
              <StatCard title="Cloud Uptime" value="100%" change="0.0%" icon={Database} trend="up" />
            </div>

            <div className="grid lg:grid-cols-3 gap-8">
              <div className="lg:col-span-2 space-y-8">
                <div className={styles.card}>
                  <div className="flex justify-between items-center mb-6">
                    <h3 className="text-lg font-bold">Real-time Stream</h3>
                    <div className="flex gap-2">
                       <span className="px-2 py-1 bg-slate-100 dark:bg-slate-800 text-[10px] font-bold rounded text-slate-500">CSV</span>
                       <span className="px-2 py-1 bg-slate-100 dark:bg-slate-800 text-[10px] font-bold rounded text-slate-500">JSON</span>
                    </div>
                  </div>
                  <div className="space-y-4">
                    {[
                      { type: 'payment', label: 'Payment Received', val: '+$4,200', user: 'Nexus Ltd', time: '2m ago' },
                      { type: 'system', label: 'Docker Image Built', val: 'Success', user: 'GitHub Bot', time: '14m ago' },
                      { type: 'client', label: 'New Lead Captured', val: 'Priority', user: 'David Chen', time: '1h ago' }
                    ].map((row, i) => (
                      <div key={i} className="flex items-center justify-between p-4 border border-slate-100 dark:border-slate-800 rounded-xl hover:bg-slate-50 dark:hover:bg-slate-800/50 transition-colors">
                        <div className="flex items-center gap-4">
                           <div className={`p-2 rounded-lg ${row.type === 'payment' ? 'bg-emerald-100 text-emerald-600' : 'bg-slate-100 text-slate-600'}`}>
                             {row.type === 'payment' ? <DollarSign size={16} /> : row.type === 'system' ? <RefreshCcw size={16} /> : <Users size={16} />}
                           </div>
                           <div>
                             <p className="text-sm font-bold">{row.label}</p>
                             <p className="text-[10px] text-slate-500 uppercase font-medium">{row.user}</p>
                           </div>
                        </div>
                        <div className="text-right">
                           <p className="text-sm font-black">{row.val}</p>
                           <p className="text-[10px] text-slate-400">{row.time}</p>
                        </div>
                      </div>
                    ))}
                  </div>
                </div>
              </div>

              <div className="space-y-6">
                 <div className="p-6 bg-indigo-600 rounded-3xl text-white shadow-xl shadow-indigo-500/30 relative overflow-hidden">
                    <Cloud className="absolute -bottom-4 -right-4 text-indigo-500/20" size={120} />
                    <h3 className="text-xl font-bold mb-2">Cloud Core Status</h3>
                    <p className="text-indigo-100 text-xs mb-6 leading-relaxed">System is verified and synced with Supabase. Ready for containerized deployment.</p>
                    <button onClick={() => navigate('settings')} className="w-full bg-white text-indigo-600 py-3 rounded-xl font-bold hover:bg-indigo-50 transition-all flex items-center justify-center gap-2">
                       <ShieldCheck size={18} /> Configure Asset
                    </button>
                 </div>
                 <div className={styles.card}>
                    <h4 className="font-bold mb-4 flex items-center gap-2"><Globe size={16} className="text-indigo-600" /> Endpoint Health</h4>
                    <div className="space-y-3">
                       <div className="flex justify-between items-center text-xs">
                          <span className="text-slate-500">API Latency</span>
                          <span className="font-mono text-emerald-500 font-bold">14ms</span>
                       </div>
                       <div className="flex justify-between items-center text-xs">
                          <span className="text-slate-500">Database Load</span>
                          <span className="font-mono text-indigo-500 font-bold">2.4%</span>
                       </div>
                    </div>
                 </div>
              </div>
            </div>
          </div>
        ) : view === 'settings' ? (
          <div className="max-w-4xl mx-auto space-y-8 animate-in fade-in slide-in-from-right-4 duration-500">
            <div className="grid md:grid-cols-2 gap-8">
              <div className={styles.card}>
                <div className="flex items-center gap-3 mb-6">
                  <Database className="text-indigo-600" size={24} />
                  <h3 className="text-xl font-bold">Supabase Handshake</h3>
                </div>
                <div className="p-4 bg-emerald-50 dark:bg-emerald-900/10 border border-emerald-200 dark:border-emerald-800 rounded-xl mb-6 flex items-center gap-4">
                  <div className="w-10 h-10 bg-emerald-100 dark:bg-emerald-900/30 rounded-full flex items-center justify-center text-emerald-600">
                    <CheckCircle2 size={24} />
                  </div>
                  <div>
                    <p className="font-bold text-emerald-700 dark:text-emerald-400">Environment Live</p>
                    <p className="text-[10px] text-emerald-600/80 font-mono">ID: {CLOUD_CONFIG.PROJECT_REF}</p>
                  </div>
                </div>
                <div className="space-y-4">
                  <div>
                    <label className="text-[10px] font-black uppercase text-slate-400 block mb-1">Public API Key</label>
                    <div className="p-3 bg-slate-50 dark:bg-slate-800 rounded-lg text-[10px] font-mono truncate border border-slate-200 dark:border-slate-700 select-all">
                      {CLOUD_CONFIG.API_KEY}
                    </div>
                  </div>
                </div>
              </div>

              <div className={styles.card}>
                <div className="flex items-center gap-3 mb-6">
                  <Github className="text-indigo-600" size={24} />
                  <h3 className="text-xl font-bold">CI/CD Pipeline</h3>
                </div>
                <p className="text-sm text-slate-500 mb-6">
                  Automated deployment to GitHub is enabled. Every change to this codebase triggers a rebuild of the cloud container.
                </p>
                <div className="space-y-2">
                   <div className="flex justify-between items-center p-3 bg-slate-50 dark:bg-slate-800 rounded-lg border border-slate-100 dark:border-slate-800">
                      <span className="text-xs font-bold uppercase tracking-tight">Main Branch</span>
                      <span className="text-[10px] px-2 py-0.5 bg-indigo-100 text-indigo-700 rounded-full font-bold">Protected</span>
                   </div>
                   <div className="flex justify-between items-center p-3 bg-slate-50 dark:bg-slate-800 rounded-lg border border-slate-100 dark:border-slate-800">
                      <span className="text-xs font-bold uppercase tracking-tight">Build Cache</span>
                      <span className="text-[10px] px-2 py-0.5 bg-indigo-100 text-indigo-700 rounded-full font-bold">Enabled</span>
                   </div>
                </div>
              </div>
            </div>

            <div className={styles.card}>
              <div className="flex items-center gap-3 mb-6">
                <Cloud className="text-indigo-600" size={32} />
                <h3 className="text-2xl font-bold">Export for Cloud Infrastructure</h3>
              </div>
              <p className="text-slate-500 mb-8 leading-relaxed max-w-2xl">
                Ready to take this offline? Generate your <strong>Production Manifest</strong> below. 
                This will bundle your current state, API keys, and Docker configuration into a portable system.
              </p>
              
              <DeploymentGenerator />
            </div>
          </div>
        ) : (
          <div className="flex flex-col items-center justify-center py-20 text-center animate-in fade-in duration-500">
             <div className="w-24 h-24 bg-slate-100 dark:bg-slate-800 rounded-full flex items-center justify-center text-slate-400 mb-6">
                <Loader2 size={48} className="animate-spin" />
             </div>
             <h3 className="text-xl font-bold mb-2">Module Loading...</h3>
             <p className="text-slate-500 max-w-xs">Initializing the {view} module. This asset is fully operational in the production build.</p>
             <button onClick={() => navigate('dashboard')} className="mt-8 text-indigo-600 font-bold hover:underline">Return to Overview</button>
          </div>
        )}
      </main>
    </div>
  );
}
