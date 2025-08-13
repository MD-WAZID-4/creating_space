document.getElementById('submitBtn_3').addEventListener('click', function() {
  // Get all time-slot-1 elements
  const firstSlots = document.querySelectorAll('.time-slot-1');
  
  firstSlots.forEach((slot, index) => {
    // Get status from time-slot-1
    const statusDiv1 = slot.nextElementSibling;
    if (!statusDiv1 || !statusDiv1.classList.contains('status-div-1')) return;
    
    const status = statusDiv1.textContent;
    
    // Find corresponding time-slot-2 (same row)
    const row = slot.closest('.content-row');
    const timeSlot2 = row.querySelector('.time-slot-2');
    if (!timeSlot2) return;
    
    // Remove existing status-div-2 if present
    const existingStatus2 = timeSlot2.nextElementSibling;
    if (existingStatus2 && existingStatus2.classList.contains('status-div-2')) {
      existingStatus2.remove();
    }
    
    // Create new status-div-2
    const statusDiv2 = document.createElement('div');
    statusDiv2.className = 'status-div-2';
    statusDiv2.textContent = status;
    statusDiv2.dataset.status = status.toLowerCase();
    timeSlot2.insertAdjacentElement('afterend', statusDiv2);
  });




  int n=s.size();
string a;
string b;
int ans=0;

unordered<map>mp;
priority_queue<int>pq;

if(x>y){


for(int i=0;i<n-1;i++){
    string v;
    v.push_back(s[i]);
    v.push_back(s[i+1]);
    if(v=="ab"){

        ans+=x;
    }
    else{
        a.push_back(s[i]);

    }
}



}
else{

    for(int i=0;i<n-1;i++){
    string v;
    v.push_back(s[i]);
    v.push_back(s[i+1]);
    if(v=="ba"){

        ans+=y;
    }
    else{
        a.push_back(s[i]);

    }
}

}
  
  // Visual feedback
  const copyBtn = document.getElementById('copyBtn');
  copyBtn.textContent = 'Copied!';
  setTimeout(() => {
    copyBtn.textContent = 'Copy Status to Slot 2';
  }, 2000);
});



