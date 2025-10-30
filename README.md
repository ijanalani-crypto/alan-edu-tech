# alan-edu-tech
Official website of ALAN – Education and Technology
https://github.com/ijanalani-crypto/alan-edu-tech.git
git clone https://github.com/ijanalani-crypto/alan-edu-tech.git
cd alan-edu-tech
/*
ALAN - Multipage React website (src/App.jsx + pages in single file)

This single-file React app uses:
- React Router (react-router-dom)
- Tailwind CSS (use the CDN for quick preview or install properly)
- Framer Motion for subtle animations
- A functional contact form using Formspree (no backend required)

How to use (quick):
1. Create a React app (Vite recommended):
   npm create vite@latest my-alan-site --template react
   cd my-alan-site
2. Install dependencies:
   npm install react-router-dom framer-motion
3. Tailwind quick preview (dev only): add to index.html inside <head>:
   <script src="https://cdn.tailwindcss.com"></script>
   For production use, install and configure Tailwind properly.
4. Replace src/App.jsx with this file content. Create src/main.jsx as Vite default or keep your existing entry.
5. Run the dev server: npm run dev

Formspree setup for contact form:
- Go to https://formspree.io, create a form to get your FORM_ID.
- Replace the FORMSPREE_URL constant below with the action URL from Formspree (example: "https://formspree.io/f/xxxxx").

Hosting recommendations:
- Vercel or Netlify (both offer continuous deploy from GitHub). Connect your repo and deploy.
- If you want, I can prepare the GitHub repo structure and a zip for upload.

Customize:
- Replace placeholder images with your assets.
- Edit colors in the `brand` object below.
- Add additional routes/pages as needed.

*/

import React from 'react';
import { BrowserRouter as Router, Routes, Route, Link } from 'react-router-dom';
import { motion } from 'framer-motion';

// ====== CONFIG ======
const FORMSPREE_URL = 'https://formspree.io/f/your_form_id_here'; // <- replace with your Formspree action URL
const brand = {
  primary: 'bg-blue-600',
  primaryText: 'text-white',
  accentHex: '#2563eb',
};
// ====================

export default function App() {
  return (
    <Router>
      <div className="min-h-screen bg-white text-gray-900 antialiased">
        <Header />

        <main className="max-w-6xl mx-auto px-6 py-12">
          <Routes>
            <Route path="/" element={<Home />} />
            <Route path="/about" element={<About />} />
            <Route path="/services" element={<Services />} />
            <Route path="/contact" element={<Contact />} />
            <Route path="*" element={<NotFound />} />
          </Routes>
        </main>

        <Footer />
      </div>
    </Router>
  );
}

function Header() {
  return (
    <header className={`shadow ${brand.primary}`}>
      <div className="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
        <Link to="/" className="flex items-center space-x-3 text-white">
          <div className="w-10 h-10 bg-white/20 rounded-full flex items-center justify-center font-bold">AL</div>
          <div>
            <h1 className="font-semibold text-lg">ALAN</h1>
            <p className="text-xs opacity-90">Education • Technology</p>
          </div>
        </Link>

        <nav className="hidden md:flex items-center space-x-6 text-white">
          <NavLink to="/">Accueil</NavLink>
          <NavLink to="/about">À propos</NavLink>
          <NavLink to="/services">Services</NavLink>
          <NavLink to="/contact">Contact</NavLink>
          <a href="#" className="ml-4 px-4 py-2 bg-white/20 rounded-md text-sm">Se connecter</a>
        </nav>

        <div className="md:hidden">
          {/* Simple mobile menu trigger - for production add real mobile menu */}
          <MobileMenu />
        </div>
      </div>
    </header>
  );
}

function NavLink({ to, children }) {
  return (
    <Link to={to} className="hover:underline">
      {children}
    </Link>
  );
}

function MobileMenu() {
  return (
    <details className="relative">
      <summary className="list-none p-2 rounded-md bg-white/10 text-white">☰</summary>
      <div className="absolute right-0 mt-2 w-48 bg-white rounded-md shadow p-3 text-gray-800">
        <Link to="/" className="block py-2">Accueil</Link>
        <Link to="/about" className="block py-2">À propos</Link>
        <Link to="/services" className="block py-2">Services</Link>
        <Link to="/contact" className="block py-2">Contact</Link>
      </div>
    </details>
  );
}

// ---------- Pages ----------
function Home() {
  return (
    <motion.section initial={{ opacity: 0, y: 6 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.5 }}>
      <div className="grid md:grid-cols-2 gap-8 items-center">
        <div>
          <h2 className="text-4xl md:text-5xl font-extrabold leading-tight">ALAN — Apprendre la technologie autrement</h2>
          <p className="mt-4 text-lg text-gray-700">Formations pratiques, parcours guidés et outils conçus pour rendre la tech accessible à tous. Cours en ligne, ateliers, et support personnalisé.</p>

          <div className="mt-6 flex flex-wrap gap-4">
            <Link to="/services" className={`inline-block px-6 py-3 ${brand.primary} ${brand.primaryText} rounded-full shadow`}>Nos services</Link>
            <Link to="/contact" className="inline-block px-6 py-3 border border-gray-200 rounded-full">Nous contacter</Link>
          </div>

          <div className="mt-8 grid grid-cols-3 gap-4">
            <Stat label="Heures de cours" value="120+" />
            <Stat label="Étudiants" value="2k+" />
            <Stat label="Formations" value="30+" />
          </div>
        </div>

        <div>
          <div className="rounded-2xl overflow-hidden shadow-lg">
            <img src="https://images.unsplash.com/photo-1584697964154-6b0d7a2f3a38?q=80&w=1400&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="Learning" className="w-full h-80 object-cover" />
          </div>
        </div>
      </div>
    </motion.section>
  );
}

function About() {
  return (
    <motion.section initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ duration: 0.4 }}>
      <div className="space-y-6">
        <SectionTitle title="À propos d'ALAN" />

        <div className="grid md:grid-cols-2 gap-8 items-center">
          <p className="text-gray-700">ALAN est une plateforme dédiée à l'apprentissage de compétences technologiques modernes : développement web, data, IA, et plus encore. Nous croyons en une pédagogie basée sur la pratique, les projets réels et le mentorat personnalisé.</p>

          <div className="space-y-3">
            <Feature emoji="🎯" title="Mission" desc="Rendre la tech accessible et pertinente pour les communautés locales." />
            <Feature emoji="🧑‍🏫" title="Méthode" desc="Cours pratiques, projets réels et évaluation continue." />
            <Feature emoji="🌍" title="Impact" desc="Formation de talents locaux pour le marché digital." />
          </div>
        </div>
      </div>
    </motion.section>
  );
}

function Services() {
  const cards = [
    { title: 'Formations en ligne', desc: 'Parcours structurés avec projets pratiques et certifications.', img: 'https://images.unsplash.com/photo-1555949963-aa79dcee981d?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder' },
    { title: 'Ateliers présentiels', desc: 'Ateliers intensifs pour maîtriser des compétences clés.', img: 'https://images.unsplash.com/photo-1555066931-4365d14bab8c?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder' },
    { title: 'Accompagnement pro', desc: 'Mentorat, aide à l'emploi et projets en entreprise.', img: 'https://images.unsplash.com/photo-1542744173-8e7e53415bb0?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder' },
  ];

  return (
    <motion.section initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ duration: 0.4 }}>
      <SectionTitle title="Nos services" />

      <div className="grid md:grid-cols-3 gap-6">
        {cards.map((c) => (
          <ServiceCard key={c.title} {...c} />
        ))}
      </div>
    </motion.section>
  );
}

function Contact() {
  return (
    <motion.section initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ duration: 0.4 }}>
      <SectionTitle title="Contactez-nous" />

      <div className="grid md:grid-cols-2 gap-8 items-start">
        <div>
          <p className="text-gray-700">Tu as une question ? Un projet ? Laisse-nous un message et notre équipe te répondra rapidement.</p>

          <div className="mt-6 space-y-4">
            <ContactInfo emoji="📍" title="Adresse" text="Lomé, Togo" />
            <ContactInfo emoji="✉️" title="Email" text="contact@alan.example" />
            <ContactInfo emoji="📞" title="Téléphone" text="+228 90 00 00 00" />
          </div>
        </div>

        <form className="space-y-4 bg-gray-50 p-6 rounded-lg shadow" action={FORMSPREE_URL} method="POST">
          {/* Formspree notes: include an input named _subject or _replyto if desired */}
          <div>
            <label className="block text-sm font-medium">Nom</label>
            <input name="name" type="text" className="mt-1 block w-full rounded-md border-gray-200 shadow-sm" placeholder="Ton nom" required />
          </div>

          <div>
            <label className="block text-sm font-medium">Email</label>
            <input name="email" type="email" className="mt-1 block w-full rounded-md border-gray-200 shadow-sm" placeholder="exemple@mail.com" required />
          </div>

          <div>
            <label className="block text-sm font-medium">Message</label>
            <textarea name="message" className="mt-1 block w-full rounded-md border-gray-200 shadow-sm" rows="4" placeholder="Écris ton message..." required></textarea>
          </div>

          <div className="flex items-center justify-between">
            <button type="submit" className={`px-4 py-2 rounded-md ${brand.primary} ${brand.primaryText}`}>Envoyer</button>
            <div className="text-sm text-gray-500">Nous répondons généralement sous 2-3 jours ouvrés.</div>
          </div>
        </form>
      </div>
    </motion.section>
  );
}

function NotFound() {
  return (
    <div className="text-center py-20">
      <h2 className="text-3xl font-bold">404 — Page non trouvée</h2>
      <p className="mt-4 text-gray-600">La page que tu cherches n'existe pas.</p>
      <Link to="/" className="mt-6 inline-block">Retour à l'accueil</Link>
    </div>
  );
}

// ---------- Small components ----------
function Stat({ label, value }) {
  return (
    <div className="text-center">
      <div className="text-2xl font-bold">{value}</div>
      <div className="text-sm text-gray-500">{label}</div>
    </div>
  );
}

function SectionTitle({ title }) {
  return (
    <div className="flex items-center gap-4 mb-4">
      <div className="w-2 h-12 bg-blue-600 rounded"></div>
      <h3 className="text-2xl font-semibold">{title}</h3>
    </div>
  );
}

function Feature({ emoji, title, desc }) {
  return (
    <div className="flex items-start gap-3">
      <div className="p-3 bg-blue-50 rounded-md">{emoji}</div>
      <div>
        <div className="font-semibold">{title}</div>
        <div className="text-sm text-gray-600">{desc}</div>
      </div>
    </div>
  );
}

function ServiceCard({ title, desc, img }) {
  return (
    <motion.div whileHover={{ y: -6 }} className="bg-white rounded-xl shadow p-4 transition">
      <div className="h-40 rounded-md overflow-hidden">
        <img src={img} alt={title} className="w-full h-full object-cover" />
      </div>
      <h4 className="mt-4 font-semibold">{title}</h4>
      <p className="mt-2 text-sm text-gray-600">{desc}</p>
      <div className="mt-4">
        <Link to="/contact" className="text-sm inline-block">En savoir plus →</Link>
      </div>
    </motion.div>
  );
}

function ContactInfo({ emoji, title, text }) {
  return (
    <div className="flex items-center gap-3">
      <div className="p-3 bg-blue-50 rounded">{emoji}</div>
      <div>
        <div className="font-semibold">{title}</div>
        <div className="text-sm text-gray-600">{text}</div>
      </div>
    </div>
  );
}

function Footer() {
  return (
    <footer className="border-t py-6 mt-12">
      <div className="max-w-6xl mx-auto px-6 flex flex-col md:flex-row items-center justify-between gap-4">
        <div className="text-sm">© {new Date().getFullYear()} ALAN. Tous droits réservés.</div>
        <div className="flex items-center gap-4 text-sm">
          <a href="#">Politique de confidentialité</a>
          <a href="#">Mentions légales</a>
        </div>
      </div>
    </footer>
  );
}
