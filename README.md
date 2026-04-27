import Navbar from "@/components/site/Navbar";
import Hero from "@/components/site/Hero";
import Marquee from "@/components/site/Marquee";
import About from "@/components/site/About";
import Services from "@/components/site/Services";
import Doctors from "@/components/site/Doctors";
import WhyUs from "@/components/site/WhyUs";
import Gallery from "@/components/site/Gallery";
import Reviews from "@/components/site/Reviews";
import FAQ from "@/components/site/FAQ";
import Branches from "@/components/site/Branches";
import Appointment from "@/components/site/Appointment";
import Footer from "@/components/site/Footer";
import SEO from "@/components/SEO";

const Index = () => {
  const dentistSchema = {
    "@context": "https://schema.org",
    "@type": "Dentist",
    name: "Dantwali Dental & Implant Clinic",
    image: "https://dantwali.com/og-image.jpg",
    url: "https://dantwali.com/",
    telephone: "+91-9past-clinic",
    priceRange: "₹₹",
    description:
      "Premium implant, cosmetic and restorative dentistry in Nagpur led by Dr. Manish & Dr. Priyanka Ashtankar.",
    address: [
      {
        "@type": "PostalAddress",
        streetAddress: "Manewada Road",
        addressLocality: "Nagpur",
        addressRegion: "Maharashtra",
        postalCode: "440024",
        addressCountry: "IN",
      },
      {
        "@type": "PostalAddress",
        streetAddress: "Besa-Pipla Road",
        addressLocality: "Nagpur",
        addressRegion: "Maharashtra",
        postalCode: "440034",
        addressCountry: "IN",
      },
    ],
    geo: {
      "@type": "GeoCoordinates",
      latitude: 21.0831742,
      longitude: 79.1073969,
    },
    openingHoursSpecification: [
      {
        "@type": "OpeningHoursSpecification",
        dayOfWeek: ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"],
        opens: "10:00",
        closes: "21:00",
      },
    ],
    sameAs: [
      "https://www.google.com/maps/place/Dantwali+Dental+%26+Implant+Clinic/",
    ],
    medicalSpecialty: ["Dentistry", "CosmeticDentistry", "Orthodontic"],
    aggregateRating: {
      "@type": "AggregateRating",
      ratingValue: "4.9",
      reviewCount: "250",
    },
  };

  const websiteSchema = {
    "@context": "https://schema.org",
    "@type": "WebSite",
    name: "Dantwali Dental & Implant Clinic",
    url: "https://dantwali.com/",
  };

  return (
    <main className="bg-background text-foreground overflow-x-hidden">
      <SEO
        title="Premium Dental Implants & Cosmetic Dentistry in Nagpur"
        description="Award-winning implant, cosmetic and restorative dentistry in Nagpur. 15+ years of expertise, 10,000+ smiles transformed by Dr. Manish & Dr. Priyanka Ashtankar."
        jsonLd={[dentistSchema, websiteSchema]}
      />
      <Navbar />
      <Hero />
      <Marquee />
      <About />
      <Services />
      <Doctors />
      <WhyUs />
      <Gallery />
      <Reviews />
      <FAQ />
      <Branches />
      <Appointment />
      <Footer />
    </main>
  );
};

export default Index;
