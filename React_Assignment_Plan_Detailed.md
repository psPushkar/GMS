
# 📱 React Native Progressive Assignment Series
**Goal:** Lead a novice dev through building the mobile frontend of the Garage Management System. Each assignment introduces one screen or feature, layering core React Native, Expo, TypeScript, Redux Toolkit, and API integration skills.

---

## Prerequisites
- Node ≥ 20, Yarn / PNPM
- Expo CLI (`npm install -g expo-cli`)
- Emulator or real device

---

## Assignment 0 (Day 0) – Environment Check
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 0.1 | Install Expo CLI and create starter app `expo init garage-app` (blank TypeScript) | Setup, TS template |
| 0.2 | Run on Android/iOS simulator and physical device via Expo Go | Dev pipeline |

---

## Assignment 1 (Day 1‑2) – Folder Structure & Navigation
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 1.1 | Organize folders: `src/screens/`, `components/`, `navigation/` | Scalable layout |
| 1.2 | Add **React Navigation**: Stack Navigator wrapping a placeholder `LoginScreen` and `DashboardScreen` | Basic navigation |
| 1.3 | Configure TypeScript paths aliases (tsconfig `@components/*`) | DX improvement |

---

## Assignment 2 (Day 3‑4) – Login Screen & Form Validation
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 2.1 | Build `LoginScreen` with **React Hook Form + Zod** (email, password) | Controlled forms |
| 2.2 | On submit, call mock API (`await fakeLogin()`) and navigate to Dashboard | async/await, navigation params |
| 2.3 | Show validation errors inline | UX, validation schema |

---

## Assignment 3 (Day 5‑6) – State Management & JWT Storage
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 3.1 | Add **Redux Toolkit** store (`authSlice`) | Global state |
| 3.2 | Persist JWT using Expo **SecureStore** | Secure storage |
| 3.3 | Add Axios instance with interceptor adding JWT header | API repo pattern |

---

## Assignment 4 (Day 7‑8) – Drawer Navigation & Sidebar Menu
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 4.1 | Convert to **Drawer Navigator** after login with menu items: Requests, Customers, Inventory | Drawer config |
| 4.2 | Dynamically render menu by role from Redux state | Conditional UI |
| 4.3 | Add custom Drawer component (profile, logout button) | Component reuse |

---

## Assignment 5 (Day 9‑10) – Requests List + Pagination
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 5.1 | Create `RequestsScreen` fetching `/vehicles` from Go API via RTK Query | Data fetching, caching |
| 5.2 | Implement FlatList with infinite scroll (page/size query params) | Lists & pagination |
| 5.3 | Show shimmer placeholder while loading (use `react-native-masonry` or custom) | UX polish |

---

## Assignment 6 (Day 11‑12) – Create / Edit Vehicle Form
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 6.1 | Reuse **form component** for create & edit (modal) | DRY forms |
| 6.2 | Dropdown for `VehicleType` populated from `/vehicle-types` | Dependent dropdown |
| 6.3 | Submit to API, optimistic update in list | Mutation patterns |

---

## Assignment 7 (Day 13‑14) – Cascading Dropdowns (Country → State demo)
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 7.1 | Build demo screen with 2 dropdowns (Country, State) | Cascading selects |
| 7.2 | Fetch states on country change (onChange event) | React state, onChange |
| 7.3 | Validate both fields before submit | Form refinement |

---

## Assignment 8 (Day 15‑16) – Dashboard Charts
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 8.1 | Install **Victory Native**; create bar chart for Vehicle counts by type | Data viz |
| 8.2 | Create pie chart for revenue vs cost (dummy data) | Multiple charts |
| 8.3 | Animate chart transitions | Reanimated basics |

---

## Assignment 9 (Day 17‑18) – Offline & Error Handling
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 9.1 | Detect offline status using `expo-network`; show banner | Offline UX |
| 9.2 | Cache Requests list in AsyncStorage for offline viewing | Data persistence |
| 9.3 | Global error boundary + toast alerts (react-native-toast-message) | Robustness |

---

## Assignment 10 (Day 19‑20) – Testing
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 10.1 | Add Jest + React Native Testing Library | Unit testing |
| 10.2 | Write test for LoginScreen form validation | Component test |
| 10.3 | Write integration test for Requests fetch mock | API mocking |

---

## Assignment 11 (Day 21‑22) – OTA Updates & Build
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 11.1 | Configure **EAS Update** for OTA deployments | Continuous delivery |
| 11.2 | Build release APK/AAB (`eas build -p android`) | Production build |
| 11.3 | Create README section documenting environment setup | Documentation |

---

## Assignment 12 (Day 23‑25) – Polish & Accessibility
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 12.1 | Add dark mode theming via `useColorScheme` | Theming |
| 12.2 | Ensure buttons have `accessibilityLabel` props | A11y |
| 12.3 | Localize strings using `i18next` (English/Hindi demo) | i18n |

---

> **End result:** A fully functional, production‑ready React Native app that logs in, lists & edits vehicles, visualizes stats, handles offline mode, includes tests, and supports OTA updates—perfectly synced with the Go backend.

