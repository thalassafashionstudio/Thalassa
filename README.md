# Thalassafashionstudio
import React from "react";
git init
git add .
git commit -m "Initial commit - Thalassa Fashion Studio Website"
import React from "react";

// THALASSA FASHION STUDIO — Single-file React site
// Clean, mobile-first, green & gold theme inspired by your card.
// Tailwind CSS classes used. Replace image URLs as needed.

const BRAND = {
  name: "THALASSA",
  tagline: "THE FASHION STUDIO",
  person: "Kiara Fashion Queen",
  phone1: "+91 70 69 56 5604",
  phone2: "+91 75678 83931",
  whatsapp: "+917069565604", // wa.me compatible (no spaces)
  email: "thalassafashionstudio@gmail.com",
  insta: "thalassa_fashion_studio",
  fb: "thalassa fashion studio",
  addressLine: "GF-6, Ratnaakar Halcyon, Nr. Sunshine Party Plot, Prernatirth Derasar Road, Satelite, Jodhpur Gam, Ahmedabad, 380015",
};

// If you have a logo, place its URL below
const LOGO_URL = ""; // e.g., "/logo.png" or a hosted URL
const QR_URL = ""; // optional Instagram QR code image URL

export default function ThalassaSite() {
  return (
    <div className="min-h-screen bg-[#106c3a] text-[#f3e6bf]">
      {/* Top border frame like the card */}
      <div className="border-y-8 border-[#d4b24c]" />

      {/* NAV */}
      <header className="sticky top-0 z-40 backdrop-blur bg-[#106c3a]/80 border-b border-[#d4b24c]/40">
        <div className="mx-auto max-w-7xl px-4 py-3 flex items-center justify-between">
          <div className="flex items-center gap-3">
            <div className="h-10 w-10 rounded-xl border-2 border-[#d4b24c] grid place-items-center overflow-hidden">
              {LOGO_URL ? (
                <img src={LOGO_URL} alt="Thalassa logo" className="h-full w-full object-cover" />
              ) : (
                <span className="text-xs tracking-widest">LOGO</span>
              )}
            </div>
            <div>
              <div className="font-extrabold tracking-[0.25em]">{BRAND.name}</div>
              <div className="text-[10px] tracking-[0.25em] opacity-80">{BRAND.tagline}</div>
            </div>
          </div>
          <nav className="hidden md:flex gap-6 text-sm">
            <a href="#home" className="hover:text-white">Home</a>
            <a href="#collections" className="hover:text-white">Collections</a>
            <a href="#about" className="hover:text-white">About</a>
            <a href="#visit" className="hover:text-white">Visit Us</a>
            <a href="#contact" className="hover:text-white">Contact</a>
          </nav>
          <a
            href={`https://wa.me/${BRAND.whatsapp}`}
            className="px-3 py-2 rounded-xl bg-[#d4b24c] text-[#106c3a] font-semibold text-sm shadow"
          >
            WhatsApp
          </a>
        </div>
      </header>

      {/* HERO */}
      <section id="home" className="relative overflow-hidden">
        <div className="absolute inset-0 opacity-10 bg-[repeating-linear-gradient(45deg,_#ffffff20,_#ffffff20_10px,_transparent_10px,_transparent_20px)]" />
        <div className="mx-auto max-w-7xl px-4 py-16 grid lg:grid-cols-2 gap-8 items-center">
          <div>
            <div className="inline-flex items-center gap-2 rounded-full border border-[#d4b24c]/40 px-3 py-1 text-xs text-[#f6f1db]">
              Premium · Western · Ethnic · Occasionwear
            </div>
            <h1 className="mt-4 text-4xl md:text-5xl font-extrabold leading-tight">
              {BRAND.name} <span className="block text-2xl md:text-3xl mt-2 tracking-wide">{BRAND.tagline}</span>
            </h1>
            <p className="mt-4 text-[#f6f1db]/90">
              Curated designs handpicked by <strong>{BRAND.person}</strong>. Explore classy silhouettes, festive edits and everyday chic—all under one roof.
            </p>
            <div className="mt-6 flex flex-wrap gap-3">
              <a href="#collections" className="px-5 py-3 rounded-2xl bg-[#d4b24c] text-[#106c3a] font-semibold shadow">Shop Collections</a>
              <a href="#visit" className="px-5 py-3 rounded-2xl border border-[#d4b24c]">Store Location</a>
            </div>
            <ul className="mt-6 grid sm:grid-cols-2 gap-3 text-sm text-[#f6f1db]">
              <li>✓ New arrivals every week</li>
              <li>✓ Sizes XS–XXL (custom fit available)</li>
              <li>✓ In-store styling assistance</li>
              <li>✓ Secure payments & easy exchanges</li>
            </ul>
          </div>
          <div className="bg-[#0f5f34] rounded-2xl border border-[#d4b24c]/40 shadow p-6">
            <div className="aspect-video rounded-xl bg-[#0b4e2a] grid place-items-center overflow-hidden">
              {/* Replace with a hero image */}
              <span className="opacity-75">Add your banner image here</span>
            </div>
            <div className="mt-4 flex items-center justify-between">
              <div className="text-sm opacity-80">Follow us on Instagram</div>
              <a href={`https://instagram.com/${BRAND.insta}`} className="underline">@{BRAND.insta}</a>
            </div>
          </div>
        </div>
      </section>

      {/* COLLECTIONS */}
      <section id="collections" className="bg-[#0f5f34] border-y border-[#d4b24c]/40">
        <div className="mx-auto max-w-7xl px-4 py-16">
          <h2 className="text-2xl md:text-3xl font-bold tracking-wide">Collections</h2>
          <p className="mt-2 opacity-90">Western Tops • Co-ord Sets • Dresses • Handbags • Festive Wear</p>
          <div className="mt-8 grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
            {[
              { t: "Western Tops", d: "Trendy cuts & breathable fabrics" },
              { t: "Co-ord Sets", d: "Matchy comfort for all-day chic" },
              { t: "Dresses", d: "From brunch to ballroom" },
              { t: "Handbags", d: "Statement pieces & everyday totes" },
              { t: "Ethnic / Festive", d: "Elegance for special moments" },
              { t: "Accessories", d: "Finish the look with finesse" },
            ].map((c, i) => (
              <article key={i} className="rounded-2xl border border-[#d4b24c]/40 bg-[#106c3a] shadow hover:shadow-lg transition">
                <div className="aspect-[4/3] bg-[#0b4e2a] rounded-t-2xl" />
                <div className="p-5">
                  <h3 className="font-semibold">{c.t}</h3>
                  <p className="text-sm opacity-90 mt-1">{c.d}</p>
                </div>
              </article>
            ))}
          </div>
        </div>
      </section>

      {/* ABOUT */}
      <section id="about" className="mx-auto max-w-7xl px-4 py-16">
        <div className="grid lg:grid-cols-3 gap-8 items-start">
          <div className="lg:col-span-2">
            <h2 className="text-2xl md:text-3xl font-bold">About Us</h2>
            <p className="mt-3 opacity-95 leading-7">
              At THALASSA, we believe fashion should feel effortless. Our studio curates
              contemporary designs with premium fabrics and flattering fits. Visit us for a
              personalized styling experience and discover pieces that speak your style.
            </p>
            <ul className="mt-4 list-disc pl-6 space-y-1 opacity-95">
              <li>Expert curation by {BRAND.person}</li>
              <li>Custom alterations available</li>
              <li>Gift cards & occasion styling</li>
            </ul>
          </div>
          <div className="rounded-2xl border border-[#d4b24c]/40 bg-[#0f5f34] p-6">
            <h3 className="font-semibold">Quick Info</h3>
            <div className="mt-3 text-sm space-y-2 opacity-95">
              <p>📍 {BRAND.addressLine}</p>
              <p>🕒 Mon–Sun: 11 AM – 9 PM</p>
              <p>📞 {BRAND.phone1} | {BRAND.phone2}</p>
              <p>✉️ {BRAND.email}</p>
              <p>🛜 Instagram: @{BRAND.insta}</p>
            </div>
          </div>
        </div>
      </section>

      {/* VISIT US */}
      <section id="visit" className="bg-[#0f5f34] border-y border-[#d4b24c]/40">
        <div className="mx-auto max-w-7xl px-4 py-16 grid lg:grid-cols-2 gap-8 items-start">
          <div>
            <h2 className="text-2xl md:text-3xl font-bold">Visit Our Studio</h2>
            <p className="mt-2 opacity-95">{BRAND.addressLine}</p>
            <div className="mt-6 flex flex-wrap gap-3">
              <a
                href={`tel:${BRAND.phone1.replace(/\s/g, "")}`}
                className="px-4 py-2 rounded-xl bg-[#d4b24c] text-[#106c3a] font-semibold"
              >
                Call {BRAND.phone1}
              </a>
              <a
                href={`https://wa.me/${BRAND.whatsapp}`}
                className="px-4 py-2 rounded-xl border border-[#d4b24c]"
              >
                WhatsApp Us
              </a>
            </div>
            <div className="mt-6 text-sm opacity-90">
              Parking available · Wheelchair accessible · Air-conditioned
            </div>
          </div>
          <div className="rounded-2xl overflow-hidden border border-[#d4b24c]/40 bg-[#0b4e2a]">
            {/* Replace with Google Map embed image or iframe */}
            <div className="aspect-video grid place-items-center">
              <span className="opacity-75">Add Map / Store Photo</span>
            </div>
          </div>
        </div>
      </section>

      {/* CONTACT */}
      <section id="contact" className="mx-auto max-w-7xl px-4 py-16">
        <div className="grid lg:grid-cols-3 gap-8">
          <div className="lg:col-span-2">
            <h2 className="text-2xl md:text-3xl font-bold">Get in Touch</h2>
            <p className="mt-2 opacity-90">Questions about sizes, availability or styling? Message us and we’ll respond shortly.</p>
            <form
              className="mt-6 grid gap-4 max-w-xl"
              action={`mailto:${BRAND.email}`}
              method="post"
              encType="text/plain"
            >
              <input className="bg-[#0f5f34] border border-[#d4b24c]/40 rounded-xl px-4 py-3 placeholder-[#f6f1db]/60" name="Name" placeholder="Your name" required />
              <input className="bg-[#0f5f34] border border-[#d4b24c]/40 rounded-xl px-4 py-3 placeholder-[#f6f1db]/60" name="Phone" placeholder="Phone" required />
              <input className="bg-[#0f5f34] border border-[#d4b24c]/40 rounded-xl px-4 py-3 placeholder-[#f6f1db]/60" name="Email" placeholder="Email (optional)" />
              <textarea className="bg-[#0f5f34] border border-[#d4b24c]/40 rounded-xl px-4 py-3 placeholder-[#f6f1db]/60" rows={4} name="Message" placeholder="How can we help?" required />
              <button className="px-5 py-3 rounded-2xl bg-[#d4b24c] text-[#106c3a] font-semibold shadow w-fit">Send</button>
            </form>
          </div>
          <aside className="rounded-2xl border border-[#d4b24c]/40 bg-[#0f5f34] p-6">
            <h3 className="font-semibold">Connect</h3>
            <ul className="mt-3 space-y-2 text-sm">
              <li>📞 {BRAND.phone1} | {BRAND.phone2}</li>
              <li>✉️ {BRAND.email}</li>
              <li>📸 Instagram: <a className="underline" href={`https://instagram.com/${BRAND.insta}`}>@{BRAND.insta}</a></li>
              <li>📘 Facebook: {BRAND.fb}</li>
            </ul>
            {QR_URL && (
              <div className="mt-4">
                <img src={QR_URL} alt="Instagram QR" className="w-40 h-40 rounded-lg border border-[#d4b24c]/40" />
              </div>
            )}
          </aside>
        </div>
      </section>

      {/* FOOTER */}
      <footer className="border-t border-[#d4b24c]/40 bg-[#0f5f34]">
        <div className="mx-auto max-w-7xl px-4 py-8 flex flex-col md:flex-row items-center justify-between gap-4">
          <p className="text-sm opacity-90">© {new Date().getFullYear()} THALASSA — The Fashion Studio. All rights reserved.</p>
          <div className="flex gap-4 text-sm">
            <a href="#" className="hover:text-white">Privacy Policy</a>
            <a href="#" className="hover:text-white">Terms</a>
          </div>
        </div>
      </footer>

      {/* Floating actions */}
      <div className="fixed bottom-5 right-5 flex flex-col gap-3">
        <a
          href={`https://wa.me/${BRAND.whatsapp}`}
          className="rounded-full p-4 bg-[#25D366] text-[#0b4e2a] font-bold shadow-lg"
          aria-label="WhatsApp"
        >
          WA
        </a>
        <a href={`tel:${BRAND.phone1.replace(/\s/g, "")}`} className="rounded-full p-4 bg-[#d4b24c] text-[#0b4e2a] font-bold shadow-lg" aria-label="Call">
          Call
        </a>
      </div>

      {/* Bottom border frame */}
      <div className="border-y-8 border-[#d4b24c]" />
    </div>
  );
}
