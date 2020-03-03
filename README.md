# covid19-data
Coronavirus COVID-19 dataset for cases, deaths, recovered in the US (United States), Canada, and UK (United Kingdom).

## Case Entry Format (JSON)
```typescript
interface CaseEntry {
  date: string;                 // "3/3/2020, 3:16 AM GMT-0800"

  cases: number;                // # of new confirmed cases
  deaths: number;               // # of new deaths
  recovered: number;            // # of new recovered patients
  critical: number;             // # of new critical patients
  
  postIds: string[];            // talksub.com post IDs
  urls: string[];               // source links

  country: 'US' | 'CA' | 'GB';  // ISO 3166-1 alpha-2 country codes
  state: string;                // State abbreviation. e.g. CA for California.
  county: string | null;        // e.g. Santa Clara County
  city: string | null;          // e.g. San Jose

  lat: number;                  // Latitude. -90.0 <= lat <= 90.0
  lon: number;                  // Longitude. -180.0 <= lon <= 180.0
  locationPrecision: number;    // Location proximity radius in km
}
```
