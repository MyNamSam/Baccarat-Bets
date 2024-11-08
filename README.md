# Architecture Decision Record (ADR)

**Submitters**
- Vinit Jangir
- Tan Phu Nguyen
- Samarpan Magar
---

## Referenced Use Case(s)
**The Game Mechanics**  
This ADR focuses on the architectural design necessary to implement a fully functional mobile game based on the Baccarat card game. The key features include betting options, multiplayer functionality (CPU & user), and statistics tracking.

---

## Context
This **Architecture Decision Record** outlines the architectural decisions made for the Baccarat Bets Mobile Game. The architecture is significant as it specifies the main design decisions affecting the game's functionality, performance, and scalability. These choices are crucial to the app's smooth operation and will influence the game's development, future updates, and overall user experience.

### Architectural Significance
- The app will be designed for Android smartphones, so all decisions prioritize Android compatibility.
- UI design choices are influenced by the Bootstrap framework, though architecture considerations like navigation strategy, hardware integration, and storage solutions are still pending.

---

## Proposed Design
1. **Development Framework**
   - **Decision:** Use React Native for cross-platform development.
   - **Rationale:** React Native was chosen as it enables a single codebase usable on both Android and iOS (even though the primary target is Android), reducing development time and effort. React Native is well-suited for managing complex app states and can be used for both UI design and game logic, making it the ideal framework for this application.

2. **Navigation Strategy**
   - **Decision:** Use React Navigation to manage screen transitions.
   - **Rationale:** React Navigation provides an easy-to-implement solution for switching between game views (e.g., game screen, result screen, and statistics screen). It supports stack, tab, and drawer navigation, ensuring a flexible and seamless user experience as users switch between different app states.

3. **Hardware Integration**
   - **Decision:** None.
   - **Rationale:** No fingerprint scanner or speaker integration will be included in the current version, as there is no immediate use case for them within this project's scope.

4. **Database Storage**
   - **Decision:** None.

---

## Considerations
### Alternatives Considered
1. **Development Framework Alternatives:**
   - Ionic and Cordova were eliminated as they are better suited for hybrid apps than resource-intensive games. React Native offers better performance for game development, particularly for smooth UI rendering and responsive interactions.
   - Framework7 and NativeScript were also considered, but React Native was selected to save on development time.

2. **Navigation Alternatives:**
   - React Native Navigation was considered but rejected due to its complex setup and potential issues with platform consistency. React Navigation has a simpler API and integrates seamlessly with React Native.

3. **Storage Alternatives:** None.
4. **Hardware Alternatives:** None.

---

## Decision
### Agreed Upon Implementation Details:
- **Framework:** React Native will be the primary development framework.
- **Navigation:** React Navigation will manage navigation between screens in the game.
- **Hardware Features:** None will be used.
- **Database Features:** None will be used.

### Unresolved Issues:
- **Performance:** The impact of multiplayer functionality and potential lag during real-time gameplay needs monitoring as more players join the game.

---

## References
- [React Native Documentation](https://reactnative.dev/docs/getting-started)
- [React Navigation Documentation](https://reactnavigation.org/docs/getting-started)
