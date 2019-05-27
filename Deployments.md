**Deployment Stratergies:**  

+ **Reckless Deployment**  
Destroy the old, provision the new, don’t care for consequences.

+ **Rolling Upgrade**  
adding new code into an existing deployment. The existing deployment becomes a heterogeneous pool of old version and new version, with the end goal of slowly replacing all old instances with the new instances.

+ **Blue/Green Deployment**  
Spin up a new separate deployment for the new version, without affecting the current one. Test the new version, and once ready start routing users to the new version.
  + Deployment slots used to deploy multiple versions.
  + **BLUE** (serves all user traffic) ----> **GREEN**(Absent/Idle)
  + Gradually send more and more users from Blue to Green while continuously testing the Green environment with live traffic.
  
+ **Canary Deployment**  
Deploy the new version into production alongside the old one, carefully controlling who gets to use the new version. Monitor and tune the experiment while gradually expanding it’s population.
  + Ringed Deployment, Feature toggling, Dark features, Silent launch, A/B testing, Testing in production.
  
+ **Versioned Deployment**  
Always keep all versions alive, while letting the user choose which version to use.
